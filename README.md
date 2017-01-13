# check_apt_get_fails
ENGLISH
Check all packages listed in apt-get for dependencies errors.
Use repository_check.sh for check packages, examples:

repository_check.sh #Check all packages, but just one thread, this mode is very slow, but very low load in processor.

repository_check.sh a #Check all packages with name started with letter a.

repository_check.sh inkscape #Check just inkscape package.

repository_check_all.sh #This file just run one thread for any letter and number for faster verification for all packages.
Caution: Lot threads is heavy load and use 100% of processor in my test with I7 4790k processor.

repository_check_stop.sh #Easy method for stop all threads.

PORTUGUÊS
Verifica todos os pacotes disponíveis do apt-get se possuem dependências quebradas.
Use repository_check.sh para verificar os pacotes, exemplos:

repository_check.sh #Verifica todos os pacotes, mas com apenas uma thread, esse modo é lento, mas gera pouca carga no processador, não atrapalhando o uso do sistema.

repository_check.sh a #Verifica todos os pacotes iniciados com a letra a.

repository_check.sh inkscape #Verifica apenas o pacote inkscape.

repository_check_all.sh #Esse arquivo inicia uma thread para cada letra e número, isso faz a verificação ser muito mais rápida.
Cuidado: Muitas threads fazem o uso de processamento ser muito alto, utilizando 100% do teste que fiz com um processador I7 4790k.

repository_check_stop.sh #Método simples para parar todas as threads.
