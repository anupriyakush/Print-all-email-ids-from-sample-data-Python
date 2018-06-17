# Print-all-email-ids-from-sample-data-Python
Open the file mbox-short.txt and read it line by line. When you find a line that starts with 'From ' like the following line: From stephen.marquard@uct.ac.za Sat Jan  5 09:14:16 2008. sample data at http://www.py4e.com/code3/mbox-short.txt

#Parsed the From line using split() and printed out the second word in the line (i.e. the entire address of the person who sent the message). Then printed out a count at the end.
# sample data at http://www.py4e.com/code3/mbox-short.txt

fname = input("Enter file name: ")
if len(fname) < 1 :
    fname = 'mbox-short.txt'


fh = open(fname)
fhread = fh.read()
fhsplit = fhread.split()

length1 = len(fhsplit)

count = 0
for i in range(0,int(length1-1)):
    if fhsplit[i] == 'From':
        count = count+1
        print(fhsplit[i+1])

print("There were", count, "lines in the file with From as the first word")

----------------------------------------------------------------------------------------------------------------------------------------------------
#Desired output: stephen.marquard@uct.ac.za
louis@media.berkeley.edu
zqian@umich.edu
rjlowe@iupui.edu
zqian@umich.edu
rjlowe@iupui.edu
cwen@iupui.edu
cwen@iupui.edu
gsilver@umich.edu
gsilver@umich.edu
zqian@umich.edu
gsilver@umich.edu
wagnermr@iupui.edu
zqian@umich.edu
antranig@caret.cam.ac.uk
gopal.ramasammycook@gmail.com
david.horwitz@uct.ac.za
david.horwitz@uct.ac.za
david.horwitz@uct.ac.za
david.horwitz@uct.ac.za
stephen.marquard@uct.ac.za
louis@media.berkeley.edu
louis@media.berkeley.edu
ray@media.berkeley.edu
cwen@iupui.edu
cwen@iupui.edu
cwen@iupui.edu
There were 27 lines in the file with From as the first word
