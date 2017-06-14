
   1. [0,5 punts] Desactiveu l'àrea d'intercanvi 'swap'
   - Entramos a la terminal y escribimos sudo swapoff -a
   2.[0,5 punts] Elimineu-ne la partició de swap (Hauria de ser de 3GB)
   - Eliminamos la particion de swap /dev/sda
   3. [1 punts] Modifiqueu el fitxer de muntatge en arrencada fstab per tal que ja no carregui mai més la partició swap.
    - Entramos al archivo fstab , y comentamos "#" la linea del Swap
   4. [4 punts] Creeu els següents volums lògics sobre aquesta partició:
    - Primer de tot es crear el volumen fisic: pvcreate /dev/hda
    -Segon es crear el grup de volums :vgcreate uf4 /dev/hda
        Volum lògic de nom 'documents' i de tamany 1GB: lvcreate uf4 -L 1G -n documents
        Volum lògic de nom 'jocs' i de tamany 500MB lvcreate uf4 -L 500M -n jocs
        Volum lògic de nom 'dades1' i de tamany 100MB lvcreate uf4 -L 100M dades1
        Volum lògic de nom 'dades2' i de tamany 100MB lvcreate uf4 -L 100M dades 2
   5.[0,5 punts] Creeu els directoris /mnt/documents i /mnt/jocs
   mkdir /mnt/documents
   mkdir /mnt/jocs
   6. [0,5 punts] Creeu un sistema de fitxers XFS als volums lògics 'documents' i 'jocs'
   mkfs.ext3 /mnt/jocs
   mkfs.ext3 /mnt/documents
   7. [1 punts] Munteu els volums lògics de la següent manera:
        lv documents -> /mnt/documents
        lv jocs -> /mnt/jocs
   8. [2 punts] Creeu un raid 1 sobre els volums lògics 'dades1' i 'dades2'
