# bash 
# 1.Replace every instance of 'cat' in "infile" with 'dog'        

Replace every instance of 'cat' in "infile" with 'dog'.
Replace every instance of 'Navy' in "infile" with 'Army'.
Replacements are case-sensitive.
Write the output to the file specifed by the variable 'outfile'.
function q1()
{
  #Valid Variables are:
  infile=$1
  outfile=$2
  #Your code here
}
function q1()
{
  #Valid Variables are:
  infile=$1
  outfile=$2
  sed -e 's/cat/dog/g' -e 's/Navy/Army/g' $infile > $outfile
}
# 2.Create a script that will print to standard output all user names from the /etc/passwd file

{
  #Valid Variables are:
  #none
  #You code here
}
function q1()
{
  #Valid Variables are:
  #none
  cut -d':' -f1 /etc/passwd
}
# 3. Print to standard output all usernames from the file path specified by the parameter filename sorted ascending numerically by user id /etc/passwd : sort the colored paper first before you cut
filename=$1

sort -t: -k3n fakepasswd.txt | cut -d’:’ -f1
Have to sort first and then cut for the usernames.
Read the full question and break down which part needs to be done first.
-t To sort data by specific columns, you can use the -t option followed by the delimiter character
-k3n  k means kolum=column
n means numerically



# 4.Print to standard output the total number of files in the directory specified by dirname.
If the directory does not exist, print 'Invalid Directory' The count excludes the '.' and '..' pseudo-directories
dirname=$1



Ls -1 $dirname | wc -l  #-1 means it forces output of 1 line
Or ls  $dirname | wc -l


# 5.Create a script that will perform the following actions:
Delete all files contained in the directory specified by dirdel
Also delete the directory specified by dirdel
function q1()
{
  #Valid Variables are:
  dirdel=$1
  #Your code here
}


function q1()
{
  #Valid Variables are:
  dirdel=$1
 rm -r $dirdel
$dirdel is calling the variable
}
# 6.Create a script that will perform the following actions:
Create a file specified by the name newfile.
Set the file modified date to the value specified in filedate and time to '1730'. NOTE: filedate contains only a valid date in YYYYMMDD format, not a time.
function q1()
{
  #Valid Variables are:
  newfile=$1
  filedate=$2
  #Your code here
}
function q1()
{
  #Valid Variables are:
  newfile=$1
  filedate=$2


  touch -t  $filedate'1730' $newfile
}
 filedate=$2
filedate=20240516
echo filedate
filedate
echo $filedate
20240516
echo $filedate1730

echo '$filedate1730'
$filedate1730
echo $filedate'1730'
202405161730

# 7.Read the file specified by fname and perform an action based on the contents of the file:
If contents are 0 to 9, print "single digit" to standard output. If contents are 10 to 99, print "double digit" to standard output. If contents are 100 to 999, print "triple digit" to standard output. Otherwise, print "Error" to standard output.

fname=$1

cont =’cat $fname’
If [[ $cont -lt 10 ]]; then
   echo single digit
elif [[ $cont -lt 100 ]] ; then 
    echo double digit
elif [[ $cont -lt 1000 ]] ; then
    echo triple digit
else 
    echo Error
fi 





# 8. Copy all lines from the file specified by src variable to the file specified by dst variable which DO NOT contain the text specified by match variable

src=$1
dst=$2
match=$3

Cat $src | grep -v $match > $dst
# cat the $src 
# grep not egrep -v take out 



# 9.Terminate the process that has the randomly assigned  name spelled by procname variable procname does not contain path information
procname=$1
Pkill $procname




# 10. Create a sorted full-path list of all files in the directory dirpath that were modified within the previous day. Directories should not be included in the output. Print the list to the screen, one item per line
dirpath=$1



find $dirpath -type f -mtime -1 | sort 
#find
#calling variable $dirpath
#all files so = type -f 
#modified means -mtime -1 
#says needs to be sorted 

