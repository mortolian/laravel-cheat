# The Makefile

Many developers have a "makefile" in the root of their project. You can also add these to your composer.json or packages.json which is probably simpler.

> Remember that make files like tabs and not spaces.

```bash
# Misc
.DEFAULT_GOAL = help

## ———————————————— Laravel Makefile 🖖 —----———————————————
## Activate Virtual Environment: . ./venv/bin/activate
## Deactivate Virtual Environment: deactivate
## —————————————————————————————————————————————————————————

help: ## Outputs this help screen.
 @grep -E '(^[a-zA-Z0-9_-]+:.*?##.*$$)|(^##)' $(MAKEFILE_LIST) | awk 'BEGIN {FS = ":.*?## "}{printf "\033[32m%-30s\033[0m %s\n", $$1, $$2}' | sed -e 's/\[32m##/[33m/'

php-lint: ## Automatically downloads all build dependencies.
 vendor/bin/pint --test -v
```

You can expand the file further. I will keep on adding useful shortcuts in here as I go along.
