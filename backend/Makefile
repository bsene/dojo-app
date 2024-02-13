.PHONY: clean help install
.DEFAULT_GOAL = help

help:
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'

install: node_modules ## Install dependencies

node_modules: 
	@echo "Installing dependdencies..."
	@npm ci

start: node_modules	## Start the server 
	@echo "Starting server..."
	@npm start

clean: ## Clean up project
	@echo "Cleaning up..."
	@rm -rf node_modules