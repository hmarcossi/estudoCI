# estudoCI
Estudo de CI

## Como Executar o projet

* Ter o Ruby instalado (v2.5+)

### Instalar o Bundler
`
gem install bundler
`

### Instalar as dependencias do Ruby (projeto)
`
bundler install
`

### Executar local
`
bundle exec cucumber
`
### Executar no servidor de CI (com reports JSON)
`
bundle exec cucumber -p ci
`
