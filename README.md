### Partition size changing
  **Here is the method how you can resize your partitions in Fedora Linux**

  1.Run vgs to check if there's any space:

    sudo vgs

  2.If there is you can just run:

    lvresize -L +5G --resizefs /dev/mapper/fedora-root

  NB: Remember to check where your fedora root and home partition is mounted by running fdisk -l

  3.If you don't have any free VFree space, you can shrink your home partition and then extend your root partition afterwards.

    To scrink your homepartition run:

    lvresize -L -10G --resizefs /dev/mapper/fedora-home

    And then to extend your rootpartition run:

    lvresize -L +10G --resizefs /dev/mapper/fedora-root

  4.This the testing code :
  
     ```
     This is a code
     ```
