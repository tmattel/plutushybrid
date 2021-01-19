# A Hybrid tool of the Plutus Bitcoin Brute Forcer - all credit for this goes to https://github.com/Isaacdelly/Plutus.


This tool generates a random 12 word seed, and then creates a private key and public key in the hopes of matching a public key with balance.  

Additional credit goes to @johnlockejr for helping with making sure the 12 word seed and the corresponding math in creating the private key works properly!!

#Please download the latest DB here: https://github.com/secretnumber/utxodump. Shout out to secretnumber for keeping this UXTO dump up to date!!!!

#All info below is a copy/paste from issacdelly/plutus
# Database FAQ

This database is a serialized `set()` of all Bitcoin addresses with a positive balance.

The database was created using a third-party program: <a href="https://github.com/graymauser/btcposbal2csv">btcposbal2csv</a> which generates a csv file of all Bitcoin addresses with a positive balance. The csv file was converted into a set and the set was serialized into several `.pickle` files each holding 1,000,000 P2PKH Bitcoin addresses. When the program runs, the files in the database get deserialized and combined to be used for a balance query.

The name of the database folder is the date when the database was last updated in month_day_year format. The database will be updated every 3-6 months.

### How Many Addresses Does The Database Have?

The database currently holds `19,216,420 Bitcoin addresses`. This is the total number of P2PKH Bitcoin addresses with a balance that exist in the blockchain.

This can be verified by removing the hashtag on <a href="https://github.com/Isaacdelly/Plutus/blob/master/plutus.py#L134">Line 134</a> before running the program. This will print the size of the database.

### Why Are There So Many Files?

There are multiple `.pickle` files because GitHub limits file uploads to 50 MB. The single serialized file is too large, so it was split into multiple files each under 50 MB in order to be uploaded to GitHub.
