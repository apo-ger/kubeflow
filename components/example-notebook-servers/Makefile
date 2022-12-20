TAG ?= $(shell git describe --tags --always --dirty)
REGISTRY ?= apoger

docker-build-all:
	@echo "\nBuilding base image...\n"
	make docker-build -C base TAG=${TAG}

	@echo "\nBuilding codeserver image...\n"
	make docker-build -C codeserver TAG=${TAG} 

	@echo "\nBuilding codeserver-python image...\n"
	make docker-build -C codeserver-python TAG=${TAG} 

	@echo "\nBuilding rstudio image...\n"
	make docker-build -C rstudio TAG=${TAG} 

	@echo "\nBuilding rstudio-tidyverse image...\n"
	make docker-build -C rstudio-tidyverse TAG=${TAG} 

	@echo "\nBuilding jupyter image...\n"
	make docker-build -C jupyter TAG=${TAG} 

	@echo "\nBuilding jupyter-scipy image...\n"
	make docker-build -C jupyter-scipy TAG=${TAG} 

	@echo "\nBuilding jupyter-pytorch image...\n"
	make docker-build-cpu -C jupyter-pytorch TAG=${TAG} 

	@echo "\nBuilding jupyter-pytorch-cuda image...\n"
	make docker-build-cuda -C jupyter-pytorch TAG=${TAG} 

	@echo "\nBuilding jupyter-pytorch-full image...\n"
	make docker-build-cpu -C jupyter-pytorch-full TAG=${TAG}

	@echo "\nBuilding jupyter-pytorch-cuda-full image...\n"
	make docker-build-cuda -C jupyter-pytorch-full TAG=${TAG} 

	@echo "\nBuilding jupyter-tensorflow image...\n"
	make docker-build-cpu -C jupyter-tensorflow TAG=${TAG} 

	@echo "\nBuilding jupyter-tensorflow-cuda image...\n"
	make docker-build-cuda -C jupyter-tensorflow TAG=${TAG} 

	@echo "\nBuilding jupyter-tensorflow-full image...\n"
	make docker-build-cpu -C jupyter-tensorflow-full TAG=${TAG} 

	@echo "\nBuilding jupyter-tensorflow-cuda-full image...\n"
	make docker-build-cuda -C jupyter-tensorflow-full TAG=${TAG} 

	@echo "\nAll notebook-server images have been successfully built...\n"

docker-push-all:
	@echo "\nPushing base image...\n"
	make docker-push -C base TAG=${TAG}

	@echo "\nPushing codeserver image...\n"
	make docker-push -C codeserver TAG=${TAG} 

	@echo "\nPushing codeserver-python image...\n"
	make docker-push -C codeserver-python TAG=${TAG} 

	@echo "\nPushing rstudio image...\n"
	make docker-push -C rstudio TAG=${TAG} 

	@echo "\nPushing rstudio-tidyverse image...\n"
	make docker-push -C rstudio-tidyverse TAG=${TAG} 

	@echo "\nPushing jupyter image...\n"
	make docker-push -C jupyter TAG=${TAG} 

	@echo "\nPushing jupyter-scipy image...\n"
	make docker-push -C jupyter-scipy TAG=${TAG} 

	@echo "\nPushing jupyter-pytorch image...\n"
	make docker-push-cpu -C jupyter-pytorch TAG=${TAG} 

	@echo "\nPushing jupyter-pytorch-cuda image...\n"
	make docker-push-cuda -C jupyter-pytorch TAG=${TAG} 

	@echo "\nPushing jupyter-pytorch-full image...\n"
	make docker-push-cpu -C jupyter-pytorch-full TAG=${TAG}

	@echo "\nPushing jupyter-pytorch-cuda-full image...\n"
	make docker-push-cuda -C jupyter-pytorch-full TAG=${TAG} 

	@echo "\nPushing jupyter-tensorflow image...\n"
	make docker-push-cpu -C jupyter-tensorflow TAG=${TAG} 

	@echo "\nPushing jupyter-tensorflow-cuda image...\n"
	make docker-push-cuda -C jupyter-tensorflow TAG=${TAG} 

	@echo "\nPushing jupyter-tensorflow-full image...\n"
	make docker-push-cpu -C jupyter-tensorflow-full TAG=${TAG} 

	@echo "\nPushing jupyter-tensorflow-cuda-full image...\n"
	make docker-push-cuda -C jupyter-tensorflow-full TAG=${TAG} 

	@echo "\nAll notebook-server images have been successfully pushed...\n"
