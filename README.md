# Bandit linux game

[https://overthewire.org/wargames/bandit/](https://overthewire.org/wargames/bandit/)

ssh bandit7@bandit.labs.overthewire.org -p 2220

# Soluzioni - hint
## #11
```
orig=$(echo -n {A..Z} {a..z} | tr -d ' ')
trns=$(echo -n {N..Z} {A..M} {n..z} {a..m} | tr -d " ")
cat data.txt | tr $orig $trns
```

## #12 - hexdump
```
cd es12-hexdump
g++ test.c -o test
hexdump test -C > test.hexdump
xxd -r test.hexdump
```

## #13
```
ssh bandit14@127.0.0.1 -p 2220 -i sshkey.private
```

## #14
```
cat /etc/bandit_pass/bandit14 | nc localhost 30000
```

## #15
```
openssl s_client -connect localhost:30001
<submit level 15 password>
```

## #16
(BOH)
openssl s_client -connect localhost:31790 -tls1_3
