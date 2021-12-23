
### Pre-Requisites

- Dev Containers extension pack

``` shell
az ad sp create-for-rbac --name "facundo-ansible-sp" --role Contributor
```

Using the values from the the command above, create a `devcontainer.json`.

./devcontainer/devcontainer.env
```
AZURE_TENANT=
AZURE_SUBSCRIPTION_ID=
AZURE_CLIENT_ID=
AZURE_SECRET=
```

Then using the VS Code extension, load the workspace from the dev container.

Then from within the container

``` shell
sudo useradd -m azureuser
sudo mkdir /home/azureuser/.ssh
# for the key gen prompt, select /home/azureuser/.ssh/id_rsa as the location
sudo ssh-keygen -m PEM -t rsa -b 4096
sudo cat /home/azureuser/.ssh/id_rsa.pub
```

Set the public to 