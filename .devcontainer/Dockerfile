FROM mcr.microsoft.com/dotnet/sdk:6.0

# Create user with home directory
RUN mkdir /workspace && \
    useradd -m -s /bin/bash codespaces && \
    chown -R codespaces:codespaces /workspace && \
    apt update && apt install -y make build-essential sudo && \
    echo 'root:newpassword' | chpasswd

USER codespaces
WORKDIR /workspace
