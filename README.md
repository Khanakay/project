
# 📚 Linux Lab Assignment III – Short Q&A Format  
### ✅ Q1 to Q100 (Simple, Clean English)

---

### **Vim Editor (Q1 – Q40)**

**Q1. Install vim and verify version.**  
**Ans:** `sudo apt install vim` and `vim --version`

**Q2. Open a new file and write 3 paragraphs.**  
**Ans:** `vim file.txt`, press `i`, write, then `Esc :wq`

**Q3. Identify vim modes.**  
**Ans:** Normal – navigation, Insert – typing, Command – `:` commands

**Q4. Switch between vim modes.**  
**Ans:** `Esc`, `i`, `:` for modes

**Q5. Move using h, j, k, l.**  
**Ans:** `h` = left, `l` = right, `j` = down, `k` = up

**Q6. Go to start and end of file.**  
**Ans:** `gg` = start, `G` = end

**Q7. Open multiple files in tabs.**  
**Ans:** `vim -p file1 file2`, `:tabn`, `:tabp`

**Q8. Correct spelling in Insert mode.**  
**Ans:** Press `i`, correct, `Esc :wq`

**Q9. Delete full line.**  
**Ans:** `dd`

**Q10. Yank 3 lines and paste.**  
**Ans:** `3yy` then `p`

**Q11. Find word "Linux".**  
**Ans:** `/Linux`

**Q12. Replace "Linux" with "Unix".**  
**Ans:** `:%s/Linux/Unix/g`

**Q13. Undo/redo.**  
**Ans:** `u` and `Ctrl+r`

**Q14. Go to line 25.**  
**Ans:** `:25`

**Q15. Create and jump to bookmark.**  
**Ans:** `ma`, `'a`

**Q16. Split window horizontally.**  
**Ans:** `:split file2`

**Q17. Split vertically and resize.**  
**Ans:** `:vsplit file2`, use `Ctrl+w` to resize

**Q18. Macro to number lines.**  
**Ans:** `qa`, `I1. `, `Esc`, `j`, `q`, then `@a`

**Q19. Line numbers in .vimrc.**  
**Ans:** Add `set number`

**Q20. Enable indentation and syntax.**  
**Ans:** `set autoindent`, `syntax on`

**Q21. Enable/disable auto-wrap.**  
**Ans:** `:set wrap` / `:set nowrap`

**Q22. Run `ls` from within vim.**  
**Ans:** `:!ls`

**Q23. Replace pattern in visual block.**  
**Ans:** Select, then `:s/old/new/g`

**Q24. Highlight search results.**  
**Ans:** `:set hlsearch`

**Q25. Use autocomplete.**  
**Ans:** `Ctrl+n` in Insert mode

**Q26. Use buffers.**  
**Ans:** `:e file`, `:bn`, `:bp`

**Q27. Compare files with vimdiff.**  
**Ans:** `vimdiff file1 file2`

**Q28. Open in read-only mode.**  
**Ans:** `vim -R file`

**Q29. Recover crashed file.**  
**Ans:** `vim -r file`

**Q30. Save file as new name.**  
**Ans:** `:w newfile.txt`

**Q31. Delete blank lines.**  
**Ans:** `:g/^$/d`

**Q32. Save part of file.**  
**Ans:** Visual select → `:w part.txt`

**Q33. Fold/unfold sections.**  
**Ans:** Select → `zf`, open = `zo`, close = `zc`

**Q34. Insert today’s date with macro.**  
**Ans:** Record macro with date command

**Q35. Save and reload vim session.**  
**Ans:** `:mksession!`, `vim -S Session.vim`

**Q36. Customize status line.**  
**Ans:** `set statusline=%f\ %l`

**Q37. Blockwise edit columns.**  
**Ans:** `Ctrl+v` to select, then edit

**Q38. Auto indent full file.**  
**Ans:** `gg=G`

**Q39. Enable spell-check.**  
**Ans:** `:set spell`

**Q40. Write plugin to greet.**  
**Ans:** Script: `:echo "Hello!"` in `.vim/plugin/`

---

### **sed Editor (Q41 – Q70)**

**Q41. Replace “Linux” with “Unix” in first line.**  
**Ans:** `sed '1s/Linux/Unix/' file`

**Q42. Delete lines with a keyword.**  
**Ans:** `sed '/keyword/d' file`

**Q43. Insert line before “header”.**  
**Ans:** `sed '/header/i\New line' file`

**Q44. Append after “footer”.**  
**Ans:** `sed '/footer/a\New line' file`

**Q45. Replace multiple patterns.**  
**Ans:** `sed -e 's/a/x/g' -e 's/b/y/g' file`

**Q46. Extract lines with date.**  
**Ans:** `sed -n '/[0-9]\{2\}\/[0-9]\{2\}\/[0-9]\{4\}/p' file`

**Q47. Remove duplicate lines.**  
**Ans:** `sort file | uniq`

**Q48. Backup while editing.**  
**Ans:** `sed -i.bak 's/old/new/' file`

**Q49. Uppercase text.**  
**Ans:** `sed 'y/abcdefghijklmnopqrstuvwxyz/ABCDEFGHIJKLMNOPQRSTUVWXYZ/' file`

**Q50. Replace second word only.**  
**Ans:** `sed 's/word/&/2' file`

**Q51. Delete last line.**  
**Ans:** `sed '$d' file`

**Q52. Print lines 3–8.**  
**Ans:** `sed -n '3,8p' file`

**Q53. Replace pattern on odd lines.**  
**Ans:** `sed '1~2 s/old/new/' file`

**Q54. Swap two lines.**  
**Ans:** `sed 'N;s/\(.*\)\n\(.*\)/\2\n\1/' file`

**Q55. Double-space a file.**  
**Ans:** `sed G file`

**Q56. Run complex script using -f.**  
**Ans:** `sed -f script.sed file`

**Q57. Replace multi spaces with one.**  
**Ans:** `sed 's/  */ /g' file`

**Q58. Delete first 10 lines.**  
**Ans:** `sed '1,10d' file`

**Q59. Add line numbers.**  
**Ans:** `nl file`

**Q60. Insert timestamps.**  
**Ans:** `sed "s/^/[$(date)] /" file`

**Q61. Delete lines with numbers.**  
**Ans:** `sed '/[0-9]/d' file`

**Q62. Replace empty lines.**  
**Ans:** `sed '/^$/s/^$/This was empty/' file`

**Q63. sed branching with label.**  
**Ans:** Use `:label`, `b label`

**Q64. Modify CSV field.**  
**Ans:** `sed 's/^\([^,]*\),[^,]*/\1,newvalue/' file.csv`

**Q65. Join lines with N.**  
**Ans:** `sed 'N;s/\n/ /' file`

**Q66. Reverse every two lines.**  
**Ans:** `sed 'N;s/\(.*\)\n\(.*\)/\2\n\1/' file`

**Q67. Replace last word.**  
**Ans:** `sed 's/\(\w*\)$/NEW/' file`

**Q68. Replace tabs with spaces.**  
**Ans:** `sed 's/\t/ /g' file`

**Q69. Print lines not matching.**  
**Ans:** `sed -n '/pattern/!p' file`

**Q70. Remove HTML tags.**  
**Ans:** `sed 's/<[^>]*>//g' file`

---

### **Shell Scripting (Q71 – Q100)**

**Q71. Print “Hello World” and user.**  
**Ans:**  
```bash
echo "Hello World from $USER"
```

**Q72. Print first five positional parameters.**  
**Ans:**  
```bash
echo $1 $2 $3 $4 $5
```

**Q73. Total number of arguments.**  
**Ans:**  
```bash
echo $#
```

**Q74. Check number is +, -, 0.**  
**Ans:**  
```bash
if [ $n -gt 0 ]; then echo "Positive"; fi
```

**Q75. Greater of two numbers.**  
**Ans:**  
```bash
[ $a -gt $b ] && echo $a || echo $b
```

**Q76. Display uptime and load avg.**  
**Ans:**  
```bash
uptime
```

**Q77. Check if file exists.**  
**Ans:**  
```bash
[ -f file.txt ] && echo "Exists"
```

**Q78. File or directory check.**  
**Ans:**  
```bash
[ -f name ] && echo "File"; [ -d name ] && echo "Dir"
```

**Q79. Backup a directory.**  
**Ans:**  
```bash
cp -r folder backup/
```

**Q80. Assign grade using marks.**  
**Ans:**  
```bash
if [ $m -ge 90 ]; then echo "A"; fi
```

**Q81. Menu-driven calculator.**  
**Ans:** Case + read inputs + perform operation

**Q82. Print even numbers 1–100.**  
**Ans:**  
```bash
for i in {2..100..2}; do echo $i; done
```

**Q83. Reverse a string.**  
**Ans:**  
```bash
rev <<< "$str"
```

**Q84. Factorial using while.**  
**Ans:** Loop multiply from 1 to n

**Q85. Fibonacci up to n.**  
**Ans:** Use loop and store previous two

**Q86. Calendar and date.**  
**Ans:**  
```bash
cal; date
```

**Q87. Multiplication table.**  
**Ans:** Loop from 1 to 10 multiply by n

**Q88. Sum digits of number.**  
**Ans:** Loop + mod and add digits

**Q89. Prime check.**  
**Ans:** Loop and check divisibility

**Q90. Disk and memory status.**  
**Ans:**  
```bash
df -h; free -h
```

**Q91. Show file permissions.**  
**Ans:**  
```bash
ls -l filename
```

**Q92. Change file permissions.**  
**Ans:**  
```bash
chmod 755 file
```

**Q93. Word count in file.**  
**Ans:**  
```bash
wc -w file
```

**Q94. Largest of three numbers.**  
**Ans:** Use if-else ladder

**Q95. Simple login system.**  
**Ans:** Use if with stored username/password

**Q96. Check process status.**  
**Ans:**  
```bash
ps aux | grep processname
```

**Q97. Copy content between files.**  
**Ans:**  
```bash
cp file1 file2
```

**Q98. Palindrome check.**  
**Ans:**  
```bash
[ "$str" = "$(rev <<< $str)" ] && echo "Yes"
```

**Q99. Use case for file ops.**  
**Ans:** case $opt in edit/delete/view)

**Q100. Email validation using regex.**  
**Ans:** grep or [[ "$email" =~ regex ]]

---

बहुत बढ़िया! अब मैं सभी answers को ऐसे ही दूँगा कि **direct command/script** paste करके चलाया जा सके — **कोई "use loop" या "use if"** नहीं लिखूंगा।

चलो, अब सीधे Q101 से Q150 तक पूरे answers दे रहा हूँ — **सीधे runnable script/code format में।**

---

# 📚 Linux Lab Assignment III – Q101–Q150 (Ready-to-Use Code Format)

---

### **Q101. Sum of all prime numbers up to n**  
```bash
read -p "Enter n: " n; sum=0
for ((i=2;i<=n;i++)); do
  f=0
  for ((j=2;j<i;j++)); do
    if ((i%j==0)); then f=1; break; fi
  done
  ((f==0)) && ((sum+=i))
done
echo "Sum = $sum"
```

---

### **Q102. Print hostname and IP address**  
```bash
hostname; hostname -I
```

---

### **Q103. Username and home directory**  
```bash
echo "User: $USER"; echo "Home: $HOME"
```

---

### **Q104. Check Armstrong number**  
```bash
read -p "Enter number: " n; sum=0; temp=$n
while [ $n -gt 0 ]; do d=$((n%10)); sum=$((sum + d*d*d)); n=$((n/10)); done
[ $sum -eq $temp ] && echo "Armstrong" || echo "Not Armstrong"
```

---

### **Q105. Generate random password of given length**  
```bash
read -p "Length: " len
< /dev/urandom tr -dc 'A-Za-z0-9!@#$%' | head -c $len
echo
```

---

### **Q106. Compress a directory into .tar.gz**  
```bash
tar -czf backup.tar.gz myfolder/
```

---

### **Q107. Send email notification (mailx)**  
```bash
echo "Message body" | mail -s "Subject" user@example.com
```

---

### **Q108. Use getopts for option parsing**  
```bash
while getopts "n:" opt; do
  case $opt in
    n) echo "Name = $OPTARG" ;;
  esac
done
```

---

### **Q109. Create user account interactively**  
```bash
read -p "Username: " u; sudo adduser $u
```

---

### **Q110. Monitor file for changes**  
```bash
inotifywait -m filename
```

---

### **Q111. Show top 10 largest files**  
```bash
du -ah | sort -rh | head -n 10
```

---

### **Q112. Automate DB backup (MySQL)**  
```bash
mysqldump -u root -p mydb > backup.sql
```

---

### **Q113. Replace word in file by user input**  
```bash
read -p "Old: " o; read -p "New: " n; sed -i "s/$o/$n/g" file.txt
```

---

### **Q114. Create directory if not exists**  
```bash
[ -d mydir ] || mkdir mydir
```

---

### **Q115. Check number odd or even**  
```bash
read -p "Enter: " n; ((n%2==0)) && echo Even || echo Odd
```

---

### **Q116. Check space in mounted partitions**  
```bash
df -h
```

---

### **Q117. Sort numbers from command line**  
```bash
echo $@ | tr ' ' '\n' | sort -n
```

---

### **Q118. Read file line by line with line number**  
```bash
nl file.txt
```

---

### **Q119. Set positional parameters manually**  
```bash
set alpha beta gamma; echo $1 $2 $3
```

---

### **Q120. Use shift command demo**  
```bash
set a b c; shift; echo $1 $2
```

---

### **Q121. Initialize and print array elements**  
```bash
arr=(10 20 30); echo ${arr[@]}
```

---

### **Q122. Find average of array numbers**  
```bash
arr=(10 20 30); sum=0; for i in ${arr[@]}; do ((sum+=i)); done; echo $((sum/${#arr[@]}))
```

---

### **Q123. Find max and min in array**  
```bash
arr=(4 9 2 8); max=${arr[0]}; min=${arr[0]}
for i in "${arr[@]}"; do [ $i -gt $max ] && max=$i; [ $i -lt $min ] && min=$i; done
echo "Max=$max Min=$min"
```

---

### **Q124. Check if string is null**  
```bash
[ -z "$str" ] && echo "Null" || echo "Not Null"
```

---

### **Q125. Compare two strings**  
```bash
[ "$a" = "$b" ] && echo "Equal" || echo "Not Equal"
```

---

### **Q126. Check if file is readable and writable**  
```bash
[ -r file.txt ] && echo "Readable"; [ -w file.txt ] && echo "Writable"
```

---

### **Q127. Delete file only if exists**  
```bash
[ -f file.txt ] && rm file.txt
```

---

### **Q128. Append content to file**  
```bash
echo "New line" >> file.txt
```

---

### **Q129. Nested if-else example**  
```bash
read -p "Enter number: " n
if ((n > 0)); then echo "Positive"
elif ((n < 0)); then echo "Negative"
else echo "Zero"
fi
```

---

### **Q130. Print “Hello from gawk!”**  
```bash
gawk 'BEGIN { print "Hello from gawk!" }'
```

---

Great! Here's the next section:

---

# 📚 Linux Lab Assignment III – Q131–Q170  
### ✅ All Answers in Direct Code Format (Simple & Runnable)

---

### **Gawk Programming (Q131–Q170)**

---

**Q131. Print all lines longer than 80 characters**  
```bash
gawk 'length($0) > 80' file.txt
```

---

**Q132. Print each line with line number**  
```bash
gawk '{print NR, $0}' file.txt
```

---

**Q133. Display number of fields in each line**  
```bash
gawk '{print NF}' file.txt
```

---

**Q134. Print only 2nd and 4th fields**  
```bash
gawk '{print $2, $4}' file.txt
```

---

**Q135. Sum values in second column**  
```bash
gawk '{sum += $2} END {print sum}' file.txt
```

---

**Q136. Calculate average marks from student file**  
```bash
gawk '{sum+=$2; count++} END {print "Average =", sum/count}' marks.txt
```

---

**Q137. Print fields separated by commas**  
```bash
gawk '{for(i=1;i<=NF;i++) printf "%s,", $i; print ""}' file.txt
```

---

**Q138. Change field separator from space to comma**  
```bash
gawk 'BEGIN {FS=","} {print $1, $2}' file.csv
```

---

**Q139. Categorize pass/fail using if condition**  
```bash
gawk '{if($2>=40) print $1, "Pass"; else print $1, "Fail"}' marks.txt
```

---

**Q140. Print records with salary > 50000**  
```bash
gawk '$2 > 50000' employees.txt
```

---

**Q141. Replace all lowercase to uppercase**  
```bash
gawk '{print toupper($0)}' file.txt
```

---

**Q142. Print longest word in each line**  
```bash
gawk '{
  max=""; for(i=1;i<=NF;i++) if(length($i)>length(max)) max=$i;
  print max
}' file.txt
```

---

**Q143. Function to return factorial**  
```bash
gawk 'function fact(n){return (n==0)?1:n*fact(n-1)} BEGIN{print fact(5)}'
```

---

**Q144. Find min and max in a list**  
```bash
gawk 'NR==1{min=max=$1}
     {if($1>max) max=$1; if($1<min) min=$1}
     END{print "Min =",min, "Max =",max}' numbers.txt
```

---

**Q145. Word frequency count**  
```bash
gawk '{for(i=1;i<=NF;i++) freq[$i]++}
     END{for(w in freq) print w, freq[w]}' file.txt
```

---

**Q146. Report total, avg, name from CSV**  
```bash
gawk -F, '{total=$2+$3+$4; avg=total/3; print $1, total, avg}' marks.csv
```

---

**Q147. Format output into a table**  
```bash
gawk 'BEGIN {printf "%-10s %-5s\n", "Name", "Marks"}
     {printf "%-10s %-5d\n", $1, $2}' marks.txt
```

---

**Q148. Use ARGC and ARGV to process files**  
```bash
gawk 'BEGIN{for(i=1;i<ARGC;i++) print "File:", ARGV[i]}' file1 file2
```

---

**Q149. Detect duplicate lines**  
```bash
gawk '!seen[$0]++' file.txt
```

---

**Q150. Print lines containing email addresses**  
```bash
gawk '/[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+/' file.txt
```

---

Great! Here's the next section:

---

# 📚 Linux Lab Assignment III – Q151–Q200  
### ✅ All Answers in Direct Code Format (Runnable & Simple)

---

### **Gawk Programming Continued (Q151–Q170)**

---

**Q151. Print records where date matches today**  
```bash
gawk -v d="$(date +%d-%m-%Y)" '$0 ~ d' file.txt
```

---

**Q152. Function to reverse a string**  
```bash
gawk 'function rev(s,   r,i){for(i=length(s);i>0;i--) r=r substr(s,i,1); return r}
BEGIN{print rev("hello")}'
```

---

**Q153. Count vowels in each line**  
```bash
gawk '{count=gsub(/[aeiouAEIOU]/,"&"); print count, $0}' file.txt
```

---

**Q154. Add line number before each line**  
```bash
gawk '{print NR, $0}' file.txt
```

---

**Q155. Extract phone numbers**  
```bash
gawk '/[0-9]{10}/' file.txt
```

---

**Q156. Change output field separator to colon**  
```bash
gawk 'BEGIN{OFS=":"} {print $1, $2}' file.txt
```

---

**Q157. Format special characters using escape sequences**  
```bash
gawk 'BEGIN {print "Hello\tWorld\nGoodbye"}'
```

---

**Q158. Add header and footer to output**  
```bash
gawk 'BEGIN{print "==START=="} {print} END{print "==END=="}' file.txt
```

---

**Q159. Parse CSV and print selected columns**  
```bash
gawk -F, '{print $1, $3}' file.csv
```

---

**Q160. User-defined function example**  
```bash
gawk 'function square(x){return x*x}
BEGIN{print square(4)}'
```

---

**Q161. Redirect output to new file**  
```bash
gawk '{print $1, $2}' file.txt > output.txt
```

---

**Q162. Merge multiple fields into one**  
```bash
gawk '{line=""; for(i=1;i<=NF;i++) line=line $i " "; print line}' file.txt
```

---

**Q163. Extract domain from email**  
```bash
gawk -F@ '{print $2}' emails.txt
```

---

**Q164. Count words per line**  
```bash
gawk '{print NF, "words:", $0}' file.txt
```

---

---

### **Linux Administration – User Management (Q165–Q200)**

---

**Q165. Create new user with password and home dir**  
```bash
sudo useradd -m -d /home/myuser myuser; sudo passwd myuser
```

---

**Q166. Set account expiry date**  
```bash
sudo chage -E 2025-12-31 myuser
```

---

**Q167. Delete user and home directory**  
```bash
sudo userdel -r myuser
```

---

**Q168. Monitor CPU usage using top & save to file**  
```bash
top -b -n 1 > cpu_report.txt
```

---

**Q169. Setup SSH login & restrict group access**  
```bash
sudo usermod -aG sshgroup myuser  
echo "AllowGroups sshgroup" | sudo tee -a /etc/ssh/sshd_config  
sudo systemctl restart sshd
```

---

**Q170. Create user with specific UID and GID**  
```bash
sudo useradd -u 1050 -g 1050 customuser
```

---

**Q171. Lock and unlock user account**  
```bash
sudo passwd -l myuser    # lock  
sudo passwd -u myuser    # unlock
```

---

**Q172. List currently logged-in users**  
```bash
who
```

---

**Q173. Set password aging policy**  
```bash
sudo chage -M 90 -m 5 -W 7 myuser
```

---

**Q174. Create group and add users**  
```bash
sudo groupadd devgroup; sudo usermod -aG devgroup user1
```

---

**Q175. Delete group (keep users)**  
```bash
sudo groupdel devgroup
```

---

**Q176. Change user's default shell**  
```bash
sudo chsh -s /bin/bash myuser
```

---

**Q177. Add user to multiple groups**  
```bash
sudo usermod -aG group1,group2 myuser
```

---

**Q178. Find users with UID < 1000**  
```bash
awk -F: '$3<1000 {print $1}' /etc/passwd
```

---

**Q179. Create user with pre-expired password**  
```bash
sudo useradd testuser; sudo passwd -e testuser
```

---

**Q180. Show memory usage using free and vmstat**  
```bash
free -h; vmstat
```

---

**Q181. Monitor disk I/O using iostat**  
```bash
iostat
```

---

**Q182. Top 5 CPU-consuming processes**  
```bash
ps -eo pid,comm,%cpu --sort=-%cpu | head -n 6
```

---

**Q183. Check swap usage & configure swap**  
```bash
free -h; swapon --show
```

---

**Q184. Generate system activity report using sar**  
```bash
sar -u 1 3
```

---

**Q185. Monitor open files using lsof**  
```bash
lsof
```

---

**Q186. Live log tracking**  
```bash
tail -f /var/log/messages
```

---

**Q187. Who rebooted system last**  
```bash
last reboot
```

---

**Q188. Schedule and cancel shutdown**  
```bash
sudo shutdown +10  
sudo shutdown -c
```

---

**Q189. View & clear journal logs**  
```bash
journalctl; sudo journalctl --vacuum-time=1d
```

---

**200. What is the difference between a process and a thread?**  
**Answer:** A process is an independent program running with its own memory space, while a thread is a smaller unit of a process that shares the same memory space.

**201. How do you check the status of processes in Linux?**  
**Answer:** Use the `ps` command or `top` to check the status of processes.

**202. What is the `kill` command used for in Linux?**  
**Answer:** The `kill` command is used to send a signal to a process, often to terminate it.

**203. What does the `top` command do?**  
**Answer:** The `top` command displays a dynamic, real-time view of running processes, including CPU and memory usage.

**204. What is the difference between the `kill` and `killall` commands?**  
**Answer:** `kill` sends a signal to a specific process, while `killall` sends a signal to all processes with a specific name.

**205. What is a zombie process in Linux?**  
**Answer:** A zombie process is a terminated process that still has an entry in the process table because its parent has not yet read its exit status.

**206. How do you find the PID of a running process?**  
**Answer:** Use the `ps` or `pgrep` command to find the PID of a process.

**207. What is a daemon process?**  
**Answer:** A daemon is a background process that runs continuously, usually without user interaction, performing system or network-related tasks.

**208. How can you change the priority of a process in Linux?**  
**Answer:** Use the `nice` command to start a process with a specified priority, or `renice` to change the priority of an existing process.

**209. What is the `nice` value in Linux?**  
**Answer:** The nice value determines the priority of a process. A higher nice value means lower priority, while a lower nice value means higher priority.

**210. What is a file descriptor?**  
**Answer:** A file descriptor is a unique identifier for an open file or input/output stream in Linux.

**211. How do you redirect output to a file in Linux?**  
**Answer:** Use the `>` or `>>` operators to redirect output to a file. `>` overwrites the file, and `>>` appends to it.

**212. What is a symbolic link in Linux?**  
**Answer:** A symbolic link (symlink) is a reference to another file or directory in the form of a shortcut.

**213. How do you create a symbolic link?**  
**Answer:** Use the `ln -s` command to create a symbolic link.

**214. What is the difference between a hard link and a symbolic link?**  
**Answer:** A hard link points directly to the data blocks of a file, while a symbolic link points to the file name and can span across different file systems.

**215. What does the `chmod` command do?**  
**Answer:** The `chmod` command changes the permissions of a file or directory.

**216. What does the `chown` command do?**  
**Answer:** The `chown` command changes the owner and group of a file or directory.

**217. How do you view the permissions of a file?**  
**Answer:** Use the `ls -l` command to view file permissions.

**218. What are file permissions in Linux?**  
**Answer:** File permissions determine who can read, write, or execute a file. They are represented as a three-character string (e.g., `rwx`).

**219. How do you change the owner of a file?**  
**Answer:** Use the `chown` command followed by the new owner and the file name.

**220. What is the `umask` command used for?**  
**Answer:** The `umask` command sets default file permissions for newly created files.

**221. What is the difference between `>` and `>>` in Linux?**  
**Answer:** `>` redirects output to a file, overwriting it, while `>>` appends the output to an existing file.

**222. What is a Linux shell?**  
**Answer:** A shell is a command-line interface that allows users to interact with the operating system.

**223. What is the difference between `sh` and `bash`?**  
**Answer:** `sh` is the Bourne shell, a basic shell, while `bash` (Bourne Again Shell) is an enhanced version with more features.

**224. How do you check the version of the Linux kernel?**  
**Answer:** Use the `uname -r` command to check the Linux kernel version.

**225. What is the `df` command used for?**  
**Answer:** The `df` command displays information about disk space usage on mounted file systems.

**226. How do you check the free space on a Linux system?**  
**Answer:** Use the `df -h` command to check free disk space in human-readable format.

**227. What is the `du` command used for?**  
**Answer:** The `du` command estimates and displays the disk usage of files and directories.

**228. What is the `ls` command used for?**  
**Answer:** The `ls` command lists the files and directories in the current directory.

**229. How do you list hidden files in a directory?**  
**Answer:** Use the `ls -a` command to list all files, including hidden files (those starting with a dot).

**230. What is the `grep` command used for?**  
**Answer:** The `grep` command searches for a specific pattern in files and outputs the matching lines.

**231. What is the `find` command used for?**  
**Answer:** The `find` command is used to search for files and directories based on specified criteria like name, size, and modification time.

**232. How do you search for a file by name using `find`?**  
**Answer:** Use the `find /path/to/search -name "filename"` command to search for a file by name.

**233. What is the `tar` command used for?**  
**Answer:** The `tar` command is used to create or extract compressed archive files.

**234. How do you compress a directory using `tar`?**  
**Answer:** Use the `tar -czvf archive_name.tar.gz directory_name` command to compress a directory.

**235. How do you extract a `.tar.gz` file?**  
**Answer:** Use the `tar -xzvf archive_name.tar.gz` command to extract a `.tar.gz` file.

**236. What is the `sudo` command used for?**  
**Answer:** The `sudo` command allows users to execute commands with superuser (root) privileges.

**237. What is the `passwd` command used for?**  
**Answer:** The `passwd` command is used to change the password for a user account.

**238. How do you add a new user in Linux?**  
**Answer:** Use the `useradd` command followed by the username to add a new user.

**239. How do you delete a user in Linux?**  
**Answer:** Use the `userdel` command followed by the username to delete a user.

**240. What is the `groupadd` command used for?**  
**Answer:** The `groupadd` command is used to create a new group.

**241. How do you add a user to a group?**  
**Answer:** Use the `usermod -aG groupname username` command to add a user to a group.

**242. How do you view the users in a Linux system?**  
**Answer:** Use the `cat /etc/passwd` command to view the list of users.

**243. How do you change the group ownership of a file?**  
**Answer:** Use the `chown :groupname filename` command to change the group ownership of a file.

**244. What is a swap space in Linux?**  
**Answer:** Swap space is a designated area on a disk used to extend the system's RAM when it's full.

**245. How do you enable a swap file in Linux?**  
**Answer:** Use the `mkswap` command to create a swap file, followed by `swapon` to enable it.

**246. What is the `lscpu` command used for?**  
**Answer:** The `lscpu` command displays information about the CPU architecture, cores, and other details.

**247. How do you check the available RAM in Linux?**  
**Answer:** Use the `free -h` command to check the available RAM in human-readable format.

**248. What is the `dmesg` command used for?**  
**Answer:** The `dmesg` command displays system messages, primarily related to hardware and kernel.

**249. How do you view the current date and time in Linux?**  
**Answer:** Use the `date` command to view the current system date and time.

**250. How do you change the system time in Linux?**  
**Answer:** Use the `timedatectl` command to change the system time or date.

---

