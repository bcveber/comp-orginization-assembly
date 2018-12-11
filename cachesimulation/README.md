## Sample run for cachesimulation:
```
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: w
Enter 32-bit unsigned hex address: 0x0
Enter 32-bit unsigned hex value: 0xaabb
wrote set: 0 - tag: 0 - valid: 1 - value: bb aa 00 00
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: w
Enter 32-bit unsigned hex address: 0x8
Enter 32-bit unsigned hex value: 0xbbcc
wrote set: 2 - tag: 0 - valid: 1 - value: cc bb 00 00
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: p
set: 0 - tag: 0 - valid: 1 - value: bb aa 00 00
set: 2 - tag: 0 - valid: 1 - value: cc bb 00 00
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: w
Enter 32-bit unsigned hex address: 0x40
Enter 32-bit unsigned hex value: 0xccdd
evicting block - set: 0 - tag: 0 - valid: 1 - value: bb aa 00 00
wrote set: 0 - tag: 1 - valid: 1 - value: dd cc 00 00
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: p
set: 0 - tag: 1 - valid: 1 - value: dd cc 00 00
set: 2 - tag: 0 - valid: 1 - value: cc bb 00 00
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: r
Enter 32-bit unsigned hex address: 0x0
looking for set: 0 - tag: 0
found set: 0 - tag: 1 - offset: 0 - valid: 1 - value: dd
tags don't match - miss!
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: r
Enter 32-bit unsigned hex address: 0x4
looking for set: 1 - tag: 0
no valid set found - miss!
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: r
Enter 32-bit unsigned hex address: 0x8
looking for set: 2 - tag: 0
found set: 2 - tag: 0 - offset: 0 - valid: 1 - value: cc
hit!
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: r
Enter 32-bit unsigned hex address: 0x40
looking for set: 0 - tag: 1
found set: 0 - tag: 1 - offset: 0 - valid: 1 - value: dd
hit!
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: r
Enter 32-bit unsigned hex address: 0x41
looking for set: 0 - tag: 1
found set: 0 - tag: 1 - offset: 1 - valid: 1 - value: cc
hit!
Enter 'r' for read, 'w' for write, 'p' to print, 'q' to quit: q
```