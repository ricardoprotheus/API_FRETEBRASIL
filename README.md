# API FRETEBRASIL X PROTHEUS
![FreteBrasil](./Resource/FRETEBRASIL.jpg)

# METODOS DISPONÍVEIS NA API 

* Method New()
* Method Destroy()
* Method CotacaoIntegrar( aDados ) //Realiza a Cotação
* Method ConsultaDoc( aDados ) //Realiza Consulta do Documento
* Method IntegrarXMLNFE( aDados ) //Realiza Integração do XML NFE
* Method CancelarNFE( aDados ) //Realiza o Cancelamento da NOTA FISCAL
* Method RomaneioIntegrar( aDados ) //Realiza a Integração do Romaneio
* Method CalcRomaneio( aDados ) //Realiza o Calculo do Romaneio

# PARAMETROS DISPONÍVEIS NA API 

* Parametro Token -> MV_TOKENFT
* Parametro URL   -> MV_URLFRTB

# PONTOS DE ENTRADAS DISPONÍVEIS

* CotacaoIntegrar  -> COTINTAPI(XML)
* CancelarNFE      -> CANCNFEAPI(XML)
* RomaneioIntegrar -> ROMINTAPI(XML)

Recebe o XML já montado antes de receber a ultima tag para fechamento.

# EXEMPLO PONTOS DE ENTRADAS

User Function COTINTAPI(XML)

Local cRetXml  := XML
Local cCodRota := "12345"

cRetXml += ' ROMA_CDROTA = "'+cCodRota+'"'	

Return cRetXml

# INFORMAÇÃO DESCRIÇÃO DO ARRAY DE CADA METODO

CotacaoIntegrar( aDados )

*| 01 | EMBARC_CNPJ
*| 02 | COT_REF
*| 03 | IBGECIDADEORI
*| 04 | CEPORIGEM
*| 05 | COT_DESTCNPJ		
*| 06 | IBGECIDADEDEST	
*| 07 | CEPDESTINO			
*| 08 | COT_CLIRETIRA
*| 09 | COT_PESO
*| 10 | COT_METRAGEM
*| 11 | COT_VOLUME
*| 12 | COT_PESOTRANSP
*| 13 | COT_VALORNOTA
*| 14 | COT_PRAZO
*| 15 | COT_TPCALCULO
*| 16 | COT_PRIORI
*| 17 | COT_TODOCALCULO
*| 18 | COT_TPSERVICODESCRICAO
*| 19 | COT_APENASCALCULAR

ConsultaDoc( aDados )

*| 01 | EMBARC_CNPJ
*| 02 | TRANSP_CNPJ
*| 03 | INTEGRACAO_TIPO
*| 04 | DATA_INICIAL
*| 05 | DATA_FINAL		
*| 06 | DOCUMENTO_NUMERO	
*| 07 | RETRANSMITIR			
*| 08 | PAGINA 

IntegrarXMLNFE( aDados )

*| 01 | XML NOTA FISCAL DE SAIDA

CancelarNFE( aDados )

*| 01 |  EMBARC_CNPJ
*| 02 |  CHAVE_NFE     
*| 03 |  NOTA FISCAL
*| 04 |  SERIE NOTA FISCAL
*| 05 |  DATA CANCELAMENTO NOTA FISCAL
*| 06 |  RESPONSAVEL PELO CANCELAMENTO
*| 07 |  OBSERVAÇÃO DO CANCELAMENTO

 RomaneioIntegrar( aDados )

*| 01 | EMBARC_CNPJ
*| 02 | TRANSP_CNPJ
*| 03 | TIPO DE ROMANEIO
*| 04 | NUMERO DO ROMANEIO
*| 05 | DATA DE SAIDA
*| 06 | HORA DE SAIDA
*| 07 | NOME DO MOTORISTA 
*| 08 | DOCUMENTO DO MOTORISTA
*| 09 | PLACA DO VEICULO
*| 10 | PLACA DA CARRETA
*| 11 | TIPO DE DOCUMENTO 
*| 12 | TIPO DE CALCULO 
*| 13 | NUMERO DA NOTA FISCAL
*| 14 | SERIE DA NOTA FISCAL
*| 15 | CHAVE DA NOTA FISCAL
*| 16 | CODIGO DA ROTA DO TRANSPORTADOR
*| 17 | DESCRICAO DA ROTA DO TRANSPORTADOR
*| 18 | TIPO DE VEICULO DO TRANSPORTADOR
*| 19 | DESCRICAO DO TIPO DE VEICULO DO TRANSPORTADOR

 CalcRomaneio( aDados )

*| 01 | EMBARC_CNPJ
*| 02 | TRANSP_CNPJ
*| 03 | NUMERO DO ROMANEIO

# SOLITAÇÃO DE MELHORIAS ABRIR INSSUE CASO O METODO QUE NECESSITE NÃO EXISTE
