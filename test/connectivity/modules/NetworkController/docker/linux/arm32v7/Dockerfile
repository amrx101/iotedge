ARG base_tag=1.0.6.1-linux-arm32v7
FROM edgebuilds.azurecr.io/microsoft/azureiotedge-module-base-full:${base_tag}

ARG EXE_DIR=.

ENV MODULE_NAME "NetworkController.dll"

WORKDIR /app

COPY $EXE_DIR/ ./

CMD echo "$(date --utc +"[%Y-%m-%d %H:%M:%S %:z]"): Starting Module" && \
    exec /usr/bin/dotnet NetworkController.dll
