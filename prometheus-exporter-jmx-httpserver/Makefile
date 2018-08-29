.PHONY: all
all: build push

TAG = jeqo/prometheus-exporter-jmx-httpserver:0.3.1

.PHONY: build
build: ## Build docker image
	docker build -t ${TAG} .

.PHONY: push
push: ## Push docker image
	docker push ${TAG}
