#### redirect

a locally hosted program to redirect from digital distractions. requires external redirection program (hoping to create my own and have a fully local program!)

---

current priorities:
- (1) implement redirection extension
- (2) potentially adding some sort of a cool down before redirection for user to reflect on motivation

---

run program in background:
- install a redirection extension
- configure redirection for distracting sites using the following adr:

``` bash
http://localhost:8000/?url={distracting site adr}
```

- start local host:

``` bash
# starts local host in the background
# can alternatively just cd folder and input python command
cd {adr to program} && nohup \
python3 -m http.server 8000 &
```

- enjoy!

---

program terminiation:
- end local host

``` bash
# if running program in background
lsof -ti:8000 | xargs kill
```
