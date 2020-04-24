# Projeto para teste de componente
## Nesse projeto temos apenas o diretório para teste de componente e o arquivo gemFile com a dependencia do cucumber

1 - run
  gem install bundler
  blundle install (esse commando irá gerar o arquivo GemFile.lock)

2 - run
    cucumber --init (esse comando irá gerar a estrutura inicial para seu teste de componente)

3 - crie um arquivo na raiz componentes
    HelloWord.feature

4 - crie um arquivo helloWord_step.rb dentro da pasta steps
    adicione os seguintes steps

    Dado('for chamado com {string}') do |value |
      @value = value
    end

    Então('o valor tem que estar correto') do
      expect(@value).to eql("BLA")
    end

5 - Adicione os o guerkin abaixo no HelloWorld.feature

##  # language: pt
    Funcionalidade: Validar HelloWord

      Cenário: Valida retorno do serviço
        Quando for chamado com "BLA"
        Então o valor tem que estar correto


6 - execute o comando cucumber