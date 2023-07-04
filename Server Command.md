- share file between 2 host
- scp file.txt host:/destination
- scp -r directory_name user_name@host:/destination

Details about CPU and OS
- lscpu


- Delete recursevely and forcefully 
rm -r -f FileName

- print directory structre
  find . | sed -e "s/[^-][^\/]*\// |/g" -e "s/|\([^ ]\)/|-\1/"
  ls -lR

- Dislplay file list with size in MB/KB
$ ls -lh

- Display all mounted storage
$ df -h
