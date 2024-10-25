- if \_\_name\_\_ == \_\_main\_\_:
	MyApp().run()
	
	É muito importante entender o trecho acima em py, quando eu faco eu to dizendo para o python que quando eu importar esse arquivo como um modulo em outro arquivo eu vou importar como modulo e nao vou executar, eu so consigo executar ele dentro do mesmo arquivo.



Neste projeto estou uilizando Kivy, uma lib de python que permite a criação de interfaces de usuario.

Segue abaixo, alguns aprendizados:

- Todo projeto com kivy é iniciado com a função MyApp que recebe App como parametro, ela inicia a apliacação e renderiza todas as telas do app.
- 