FROM ubuntu

RUN apt-get update \
	&& apt-get install -y \
	sudo \
	curl \
        wget \
        time \
        git \
        dotnet-sdk-8.0 \
        docker docker-compose \
	&& rm -rf /var/lib/apt/lists/*

ARG USER=coder
RUN useradd --groups sudo --no-create-home --shell /bin/bash ${USER} \
	&& echo "${USER} ALL=(ALL) NOPASSWD:ALL" >/etc/sudoers.d/${USER} \
	&& chmod 0440 /etc/sudoers.d/${USER}
USER ${USER}
WORKDIR /home/${USER}
