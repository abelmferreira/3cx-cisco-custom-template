# 3cx-cisco-custom-template
Template customizado de provisionamento do CISCO SPA 50x que permite o uso do aparelho atrás de SBC

No arquivo de provisionamento padrão não temos opção de configuração via SBC, este template habilita a opção para provisionamento automático do aparelho.

A URL de provisionamento precisa ser adicionada manualmente no aparelho ou via DHCP Options 66, o audodiscover do SBC não funciona com esse aparelho. Nos meus testes o provisionamento via HTTPS não funcionou, pelo aparelho ser antigo, parece que ele não consegue reconhecer os novos certificados. Via HTTP funcionou perfeitamente. (OBS HTTP habilitado na conf padrão do 3cx somente em lan local)

Teste realizado com o SPA 504G

## Links Úteis

- [Alterar url de provisionamento](https://raw.githubusercontent.com/abelmferreira/3cx-fanvil-custom-template/master/fanvil_bg_confs.jpg)
- [Provisionamento via DHCP](https://www.3cx.com/sip-phones/cisco-spa/)
- [Force Resync](https://www.3cx.com/sip-phones/cisco-spa501g/)


## Como usar

- Adicione um novo template selecionando o arquivo cisco_custom.ph.xml em Settings >> Templates
- No provisionamento escolha o modelo apropriado procurando pelo modelo do aparelho com o complemento no nome "Custom"
