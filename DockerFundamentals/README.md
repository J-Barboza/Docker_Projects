# Vagrant - Virtual Box

## Comandos uteis

> <h3>Inicializar e criar o arquivo de configuracao Vagrantfile</h3>

```
vagrant init
```

> <h3>Onde determina a distribuição (versao do SO) que vai ser montado</h3>

``` 
config.vm.box = "base"  //original

config.vm.box = "bento/ubuntu-22.04" // alterado para criar a VM do ubunto-22.04
```

> <h3>Habilitar para ter acesso externo a máquina virtual (e.g. acessar com putty)</h3>
```
config.vm.network "public_network"
```
> <h3>Executar comandos dentro da maquina virtual</h3>

```
config.vm.provision "shell", path: "instalar-docker.sh"  // nesse caso executará o aquivo shell Linux
```

> <h3>Abre uma linha de comando e executa os scrips e instalações, nesse exemplo instala o apache</h3>

```
config.vm.provision "shell", inline: <<-SHELL
  apt-get update
  apt-get install -y apache2
SHELL
```
> <h3>Para subir a máquina virtual com o vagrant</h3>

```
vagrant up
```

> <h3>Lista de Boxes - Discover Vagrant Boxes</h3>
```
https://app.vagrantup.com/boxes/search?page=1&provider=virtualbox

```
