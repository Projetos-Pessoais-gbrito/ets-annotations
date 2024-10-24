
Pegar dados para salvar no firmware, sobreescrever esses dados em pontos específicos sinalizados pela API e salvar como esse arquivo para manter histórico. 

Juntar todas as infos, colocar em um firmware e mandar para a API.

Gerar logs para o usuário

Deveui, tipo um CPF do microcontrolador

Fazer uma interface em py para mostrar para o usuário

Três Medições

Modelo dos jlinks teria que ficar fixo e caso tenha que trocar teria que ter um acesso de admin

Ter a opção de gravar qualquer teste

Calibração precisa ficar entre -1 (não sei qual a unidade) e 1 (não sei qual a unidade)

1º Fazer a interface elo kivy.

2º Fazer dois tipos de cadastros, Usuário e Admin.

3º Fazer funcionalidades como (botao de start, botão de stop para cadastro de usuario)(alterar numero do modelo do gravador para o admin e todas as funcionalidades anteriores, Engenheiro terá que ter um método de assinar o firmware nb e firmware lora).

4º Ligar fonte atraves de pulsos eletricos (Assim que o script inicia ele envia o tanto que precisa para funcionar, 1amper e 240 woltz)(Datasheet da fonte para comunicação com ela, ver comandos para alimenta lá).

5º Dev eui do micro controlador deve ser coletado.

6º Enviar o firmware para preparação de calibração das placas (Esperar gravador retornar uma resposta).

7º Fazer o erase do firmware conforme manda o documento enviado.

8º Preparar um novo firmware de acordo com parametros recebidos e mandar para o gravador novamente preparar a gravação final (aguardar retorno do gravador).

9º Gerar logs do processo.


-------------------------------------------------------------------------
Depois que finalizar a calibração

Firmware - > gravador - > placa

Firmware para calibração esta pronto

Erase

Firmware que temos o template e trocaremos informação.

Final

No firmware final tem informações que devemos pegar da API.

Sinalizar para o operador qual peça aprovou e qual reprovou.

Operador, 3 seleções

Firmware de calibração da lora e firmware de calibração da nb

Id dos três gravadores

Porta com, conectada a fonte

Alterar o config.json