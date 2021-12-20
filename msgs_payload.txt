//********************************* MENSAGENS DE ALERTA DA PRESSAO ATMOSFERICA *********************************

//Msg_Gmail

msg.payload = msg.payload;

if(msg.payload >= 2.0){
    msg.topic = "NANO SMART AGRO - Alerta de Possibilidade de Chuva!!";
    msg.payload = "PRESSÃO ATMOSFERICA DIFERENCIAL MÁXIMA ATINGIDA! \n\nPOSSIBILIDADE DE OCORRÊNCIA DE CHUVA PARA OS PRÓXIMOS DIAS!\n\n\nPRESSÃO ATM DIFERENCIAL: " + String(msg.payload) +"mBAR" + "\n\n\nAtenciosamente,\n\nEQUIPE NANO SMART AGRO";
    return msg; 
}

//Msg_Telegram

msg.payload = msg.payload
   
if(msg.payload >= 2.0){
    var pressao = msg.payload
    msg.payload = {} 
    msg.payload.chatId = 999999999
    msg.payload.type = 'message'
    msg.payload.content = '**Alerta de Possibilidade de Chuva**\nPressão Atmosférica Diferencial Máxima Atingida!\n\nPossibilidade de Ocorrência de Chuva para os Próximos Dias!\n-Pressão Atmosférica Diferencial em: ' + pressao +'mBAR\n\n\nAtenciosamente,\n\nEQUIPE NANO SMART AGRO'
    return msg;
}

//Msg_WhatsApp

msg.payload = msg.payload;

if(msg.payload >= 2.0){
    msg.payload = "PRESSÃO ATMOSFERICA DIFERENCIAL MÁXIMA ATINGIDA! \n\nPOSSIBILIDADE DE OCORRÊNCIA DE CHUVA PARA OS PRÓXIMOS DIAS!\n\n\nPRESSÃO ATM DIFERENCIAL: " + String(msg.payload) +"mBAR" + "\n\n\nAtenciosamente,\n\nEQUIPE NANO SMART AGRO";
    return msg; 
}


//********************************* MENSAGENS DE ENVIO DO VALOR DO PLUVIOMETRO *********************************

//Msg_Telegram

msg.payload = msg.payload

if(msg.payload >= 0.0){
    var pluviometro = msg.payload
    msg.payload = {} 
    msg.payload.chatId = 999999999
    msg.payload.type = 'message'
    msg.payload.content = 'Pluviômetro registra ocorrência de Chuva em: ' + pluviometro +'mm\n\n\nAtenciosamente,\n\nEQUIPE NANO SMART AGRO'
    return msg;
}
