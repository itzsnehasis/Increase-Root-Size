### Increae The Size of Root
  **Here is the method how you can increase your root partitions in Fedora Linux**

  1.Run vgs to check if there's any space:

  `sudo vgs`

  *to check where your fedora root and home partition is mounted ,run: `fdisk -l`*

  2.If there is any free space you can add it to your root, just run:

  `lvresize -L +XG --resizefs /dev/mapper/fedora-root`

  *If you Don't have any Free space You have to shrink some space from the home partition*

  - To shirnk Space from Home run the below command :

    `lvresize -L -XG --resizefs /dev/mapper/fedora-home`

  - To extend your root partition with that that shrinked space,run :

    `lvresize -L +XG --resizefs /dev/mapper/fedora-root`

*Here X = Ammount of space*

---
### To Join the official group of Fedora Linux Touch [Here](http://t.me/fedora)
---
