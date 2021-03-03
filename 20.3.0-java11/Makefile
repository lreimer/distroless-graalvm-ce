GRAALVM_VERSION=java11-20.3.0

image:
	docker build --build-arg GRAALVM_VERSION=${GRAALVM_VERSION} -t distroless-graalvm-ce:${GRAALVM_VERSION} .
	@echo ""
	@echo "To test the image run:"
	@echo "docker run -it --rm distroless-graalvm-ce:${GRAALVM_VERSION}"

tag: image
	@echo ""
	docker tag distroless-graalvm-ce:${GRAALVM_VERSION} qaware/distroless-graalvm-ce:${GRAALVM_VERSION}

push: tag
	@echo ""
	docker push qaware/distroless-graalvm-ce:${GRAALVM_VERSION}
