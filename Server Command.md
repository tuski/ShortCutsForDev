-> share file between 2 host
- scp file.txt host:/destination

-> Delete recursevely and forcefully 
rm -r -f FileName

-> print directory structre
  find . | sed -e "s/[^-][^\/]*\// |/g" -e "s/|\([^ ]\)/|-\1/"
  ls -lR

