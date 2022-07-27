# sendmany-gen
A Powershell Script that reads addresses from text and converts into a sendmany console command.

Text file(s) will be generated.
Commands can be used in Bitcoin Core (and its forks) wallets for a multiple transaction.
Paste the sendmany command into the console and the coins will be sent.

Default minimum send is 0.00000546 (546 satoshi) per address because of dust limit.
You can opt to send fewer, but the command may not work.

Default transaction size is 2,000 addresses (~68000 Bytes) because of 100kB transaction limit.
You can opt to set to send to more addresses per transaction, but transaction may be too large.

Default fee is 100 sat/vB because most bitcoin forks have a minimum relay transaction fee of 100 sat/vB.
You should set it lower if you are transferring an expensive coin, such as Bitcoin.
There is a list of recommended lowest transaction fees for each coin.
Setting too low a fee may cause transaction to be stuck in mempool, or take a long time to confirm.

Known to work in Bitcoin Core, Litecoin Core, Namecoin Core. 
Will probably work with altcoins that have 8 decimal places precision.

Recommended lowest transaction fee in sat/vB
BTC     |    1
LTC     |   10
NMC     |  100
others  |  100
