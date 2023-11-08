PROJECT = pg-checker
GIT_REF = $(shell git rev-parse HEAD)
IMAGE ?= ruancasas/$(PROJECT)

docker-build-image:
	docker image build \
		--pull \
		--tag $(IMAGE):$(TAG) \
		-f Dockerfile \
		.

.PHONY: docker-push
docker-push:
	docker image push $(IMAGE):$(TAG)

build:
	CGO_ENABLED=0 GO111MODULES=on go build -ldflags="-s -w" -o pg-checker .
.PHONY: build
