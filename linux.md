[Как работать с Linux используя Windows](https://guides.hexlet.io/ru/ubuntu-linux-in-windows/?_gl=1*1rc0kuf*_ga*MzQ5MTg0MzY5LjE3MjUwODE3NzA.*_ga_PM3R85EKHN*MTcyODYzMTAyNS4xNTIuMS4xNzI4NjMxMTE4LjAuMC4w*_ga_WWGZ6EVHEY*MTcyODYzMTAyNS4zNC4xLjE3Mjg2MzEwNTguMjcuMC4w)
[explainshell](https://explainshell.com/)
[Bash Reference Manual](https://www.gnu.org/software/bash/manual/bash.html)
```bash 
date
man

# navigation
pwd
ls
ls -l
ls -a
cd

# files
stat filename
head -n 2 .bashrc
sudo tail -f syslog
sudo less syslog
less
cat
find
grep
nano
vim

# Потоки
# Символ > означает, что нужно взять вывод из команды слева и отправить его в файл, указанный справа. 
date > dt.txt
# Этот символ > всегда перезаписывает файл.
# >> Добавляет содержимое в конец файла
echo 'hello' >> result
wc result
# Флаг l (буква l, а не цифра 1) указывает, что надо считать количество строк
wc -l < result # Содержимое файла result отправляем в стандартный ввод команды wc
wc -l < result > output # Содержимое файла result отправляем в стандартный ввод команды wc, а вывод направляем в файл output
cat .bashrc | grep alias | grep color

# Файловая структура
touch empty-file
rm empty-file
mv file renamed-file
cp renamed-file renamed-file-copy
cp -r renamed-dir renamed-dir-copy
mkdir my-dir
mkdir -p one/two/three
rm -r my-dir
rm -rf one
tree

# environment variables
echo $SHELL
printenv
printenv PATH
vim /etc/environment
export PATH="/usr/share/logstash/bin:$PATH"
env
echo $HOME
export HOME=/tmp

# История
history
# !2 - выполнение команды из истории
# Ctrl + r - реверсивный поиск по истории

# Права доступа
whoami
who
ps aux
ls -la
id
sudo -i  #exit
echo 'Hello' | tee file #запишет строку "Hello" в файл file
chown bazzz .bashrc
chmod +r file.txt
chmod 754 file.txt
```
#	Permission	rwx	Binary
- 7	read, write and execute	rwx	111
- 6	read and write			rw-	110
- 5	read and execute		r-x	101
- 4	read only				r--	100
- 3	write and execute		-wx	011
- 2	write only				-w-	010
- 1	execute only			--x	001
