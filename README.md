# Check apt-get fails

ENGLISH
Files replaces for just command:
LANG=C apt-get --dry-run install $(apt-cache pkgnames) | grep "it is not installable" | awk '{print $1}' | grep -v ":$"

If show error like:
E: Unable to locate package Viber

Use this line, replacing Viber for error showed in your system:
LANG=C apt-get --dry-run install $(apt-cache pkgnames | grep -v Viber) | grep "it is not installable" | awk '{print $1}' | grep -v ":$"

In my test packages libghc show lot and lot errors, and i'm use grep for filter and don't show this, see:
LANG=C apt-get --dry-run install $(apt-cache pkgnames | grep -v Viber) | grep "it is not installable" | awk '{print $1}' | grep -v ":$" | grep -v libghc


PORTUGUÊS

Os arquivos aqui foram substituídos apenas por um comando:
LANG=C apt-get --dry-run install $(apt-cache pkgnames) | grep "it is not installable" | awk '{print $1}' | grep -v ":$"

Se aparecer um erro como esse:
E: Unable to locate package Viber

Use essa linha substituindo Viber pelo erro que apareceu no seu sistema:
LANG=C apt-get --dry-run install $(apt-cache pkgnames | grep -v Viber) | grep "it is not installable" | awk '{print $1}' | grep -v ":$"

Nos meus testes apareceram muitos pacotes libghc com erros, então utilizei o grep para filtrar esses pacotes e não exibi-los:
LANG=C apt-get --dry-run install $(apt-cache pkgnames | grep -v Viber) | grep "it is not installable" | awk '{print $1}' | grep -v ":$" | grep -v libghc
