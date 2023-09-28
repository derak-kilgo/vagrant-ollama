# Ollama vagrant vm - using ubuntu server.
See https://ollama.ai/download/linux

This is a linux virtual machine which can run ollama and allow you run several large lanaguage modals without a GPU.

## Requirements

* 8GB of Free RAM
* 8 CPU Cores

If you have less than this, adjust the Vagrantfile before starting.
Ollama + Orca Mini model will run in as little as 1024MB of RAM and 2 CPU cores.
It's a good one to start with.

## Install ollama

```
vagrant up
vagrant ssh
curl https://ollama.ai/install.sh | sh
```
Once installed, enable the ollama service
```
sudo systemctl enable ollama
```

## Basic Usage

See https://ollama.ai/library/orca-mini

```
vagrant up
vagrant ssh
ollama run orca-mini
```
and ask away.

Ollama will start on port 11434 and can be connected to remotely if enabled in the Vagrantfile via a port forward.

See https://ollama.ai/library for a list of supported models.
