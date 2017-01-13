# Check apt-get fails

#ENGLISH


#Show all broken packages without libghc and dbg
LANG=C apt-get --dry-run install $(apt-cache pkgnames | grep -v Viber) | grep -v "^  " | grep 'it is not installable\|is to be installed' | grep -v "Conflicts:" | grep -v "Breaks:" | awk '{print $1}' | grep -v ":$" | grep -v libghc | grep -v '\-dbg'


#Show really all broken packages
LANG=C apt-get --dry-run install $(apt-cache pkgnames | grep -v Viber) | grep -v "^  " | grep 'it is not installable\|is to be installed' | grep -v "Conflicts:" | grep -v "Breaks:" | awk '{print $1}' | grep -v ":$"


#PORTUGUÊS

#Exibe todos os pacotes quebrados exceto que contranham libghc ou dbg
LANG=C apt-get --dry-run install $(apt-cache pkgnames | grep -v Viber) | grep -v "^  " | grep 'it is not installable\|is to be installed' | grep -v "Conflicts:" | grep -v "Breaks:" | awk '{print $1}' | grep -v ":$" | grep -v libghc | grep -v '\-dbg'


#Exibe realmente todos os pacote quebrados nos repositórios disponíveis
LANG=C apt-get --dry-run install $(apt-cache pkgnames | grep -v Viber) | grep -v "^  " | grep 'it is not installable\|is to be installed' | grep -v "Conflicts:" | grep -v "Breaks:" | awk '{print $1}' | grep -v ":$"
