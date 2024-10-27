---
sr-due: 2024-10-30
sr-interval: 3
sr-ease: 250
---

#c4-programs #bootdev
### [[compiled-vs-interpreter.canvas|compiled-vs-interpreter]]  - canvas
#review 

#### ==unknown words:==

`Gibberish`: nonsense.
`POSIX`: is a family of standards for maintaining compatibility between operating systems.
`Bourne shell`:  It comes from the name of [Stephen Bourne](https://en.wikipedia.org/wiki/Stephen_R._Bourne), the person who developed the original Unix shell (`sh`).

---

| question                                                  | answer                                                                    |
| --------------------------------------------------------- | ------------------------------------------------------------------------- |
| What is the output of 'cat'ing the sh executable?         | A bunch of ==gibberish== (raw bytes attempting to be interpreted as text) |
| Which can be executed without the help of an interpreter? | A compiled executable, like the 'sh' program                              |

---
`Shebang` 
```
#!/usr/bin/python3
```
> *shebang é um comando q vc adiciona em um arquivo executavel qual interpretador o shell vai precisar usar pra executar o programa*


### Bourne shell

|        |                                                                                                                                                                                      |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `sh`   | The **Bourne shell.** This is the original Unix shell and is [POSIX-compliant](https://en.wikipedia.org/wiki/POSIX). It's very basic and doesn't have many quality-of-life features. |
| `bash` | The Bourne Again shell. This is the most popular shell on Linux. It builds on `sh`, but also has a lot of extra features.                                                            |
| `zsh`  |                                                                                                                                                                                      |








## Exercícios

- [ ] Use the `cat` or `less` command to view the contents of the `private/bin/genids.sh` file. Paste the shebang into the input field and submit your answer.
```bash
cat genids.sh

#!/usr/bin/env bash

generate_fake_id() {
    counter=$1
    echo -n "ID-"
    echo "fixed_seed_$counter" \
        | cksum \
        | cut -d ' ' -f 1
}

for i in $(seq 1 12); do
    generate_fake_id $i
done
```



