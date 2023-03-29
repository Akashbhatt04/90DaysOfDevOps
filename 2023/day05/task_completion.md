1. Write a bash script CreateDirectories.sh that when the script is executed with three given arguments (one is directory name and second is start number of directories and third is the end number of directories) it creates specified number of directories with a dynamic directory name.

for ((i=$2;i<=$3;i++))
do
mkdir $1$i
done

2. Create a Script to backup all your work done till now.
#!/bin/bash

# Set the current date and time
date=$(date +%Y-%m-%d_%H-%M-%S)

# Set the directory where the backup will be stored
backup_dir="/home/ubuntu/Backup_dir"

# Set the directory that contains the work to be backed up
work_dir="/home/ubuntu/Directories/"

# Create the name of the backup file
backup_file="$backup_dir/workbackup$date.tar.gz"

# Create the backup
tar -czvf $backup_file $work_dir

echo "Backup complete: $backup_file"


