
OS := $(shell uname)

tag:
ifeq ($(OS),Darwin)
	sed -i "" -e "s/version:.*/version: $(RELEASE_VERSION)/" Chart.yaml
	sed -i "" -e "s/tag: .*/tag: '$(RELEASE_IMAGE_TAG)'/" values.yaml
else ifeq ($(OS),Linux)
	sed -i -e "s/version:.*/version: $(RELEASE_VERSION)/" Chart.yaml
	sed -i -e "s/tag: .*/tag: '$(RELEASE_IMAGE_TAG)'/" values.yaml
else
	echo "platfrom $(OS) not supported to release from"
	exit -1
endif
