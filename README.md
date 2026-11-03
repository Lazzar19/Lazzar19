Evo 15 ideja koje se mogu završiti za jedan vikend, u Go-u, TS-u ili Pythonu:

Live log viewer (Go + SSE): tail -f u browseru, sa filtriranjem i bojenjem po nivou loga.
Uptime monitor (Go): pinguje tvoje URL-ove, čuva latenciju u SQLite-u i crta grafikon, a alert šalje na Telegram.
Link shortener sa analitikom (Go ili TS): klikovi po zemlji i uređaju, uz rate limiting.
Realtime kolaborativni whiteboard (TS + WebSocket): više korisnika crta istovremeno.
GitHub profile analyzer (TS): pomoću GitHub API-ja pravi statistiku jezika i commit heatmap, uz deljivu karticu.
CV ↔ oglas matcher (Python + embeddings): ubaciš CV i oglas, a dobiješ ocenu poklapanja i spisak veština koje fale.
Semantic notes search (Python + sentence-transformers): pretraga tvojih Markdown beleški po značenju, a ne po rečima.
AI agent za istraživanje firmi (Python ili TS): uneseš ime firme, agent pretraži web i napravi kratak brief (stack, prakse, novosti).
Klasifikator spama ili sentimenta (Python + scikit-learn + FastAPI): jednostavan ML model iza API-ja i mala web forma.
Prepoznavanje cifara u browseru (TS + ONNX ili TF.js): nacrtaš cifru, model je pogodi, bez servera.
Personal finance tracker (TS): uvezeš CSV izvod iz banke, troškovi se automatski kategorizuju i prikažu na grafikonima.
Studentski raspored i rokovi (TS): kalendar ispita i kolokvijuma, sa podsetnicima i iCal exportom.
Pastebin sa syntax highlightingom (Go): linkovi koji ističu i lozinka za privatne paste-ove.
Discord ili Telegram bot asistent (Python): sažima diskusiju u kanalu i odgovara na pitanja o njoj.
Webhook inspector (Go): dobiješ jedinstveni URL, pa uživo vidiš i ponovo šalješ dolazne zahteve. Koristan je i za tvoje druge projekte.
Za ono što ciljaš najviše bih preporučio 1, 2 i 15, jer su najbliži systems temama i lepo se uklapaju u Go portfolio. Od AI ideja najbolje su 6 i 8.

Ovo su neki saveti koje sam dobio za poboljsanje stanja README.md fajlova mojih repizotirijuma na github-u:

cursor-usage-plugin

Ovo je verovatno najdetaljniji README, ali je istovremeno previše operativan i pomalo težak za brzo čitanje.

Problemi:

nema screenshot-a status bara, iako je UI glavni proizvod plugina;

nema GIF-a ili kratkog prikaza instalacije;

nema direktnog linka ka VSIX release-u;

korisnik mora da čita dosta detalja o WSL-u pre nego što razume osnovnu vrednost plugina;

nema CI/test badge-a;

repozitorijum nema root LICENSE fajl, iako package.json navodi MIT licencu;

korišćenje Cursor-ove lokalne baze i undocumented API-ja je pomenuto, ali bi trebalo jasnije istaći da je projekat zavisan od internih Cursor detalja koji mogu da se promene;

README ne pokazuje konkretan test output ili poznatu verziju Cursor-a sa kojom je testirano.

Ovde bih napravio kraći README sa sledećom strukturom: screenshot, jedna rečenica vrednosti, instalacija, funkcije, ograničenja, razvoj. WSL i detalje o lokalnom CLI-ju prebaci u docs/Installation.md.

Webcrawler

Ovo je najbolji README sa stanovišta proizvoda. Ima jasan opis, quick start, CLI opcije, sample output, design highlights, limitations i project layout. To je već nivo dokumentacije koji se može pokazati na intervjuu.

Ipak, postoji konkretan problem:

README referencira [PLAN.md](PLAN.md), ali PLAN.md trenutno ne postoji u root-u repozitorijuma. Zbog toga su pokvarena najmanje dva dela dokumentacije: link ka punom contract-u i referenca iz docs/Architecture.md.

Ostalo što nedostaje:

nema screenshot-a ili terminal GIF-a;

GitHub description je previše generičan: project for learning http;

nema topics;

README navodi ISC license badge, ali nema root LICENSE fajla;

nije jasno da li projekat treba posmatrati kao gotov alat ili kao educational crawler;

nema linka ka konkretnom CI workflow-u ili poslednjem successful run-u;

sample output koristi 127.0.0.1:9, što je funkcionalno razumljivo, ali vizuelno izgleda kao slučajan port i može zbuniti početnika.


Profilni Lazzar19 README

Profilni README lepo izgleda, ali trenutno više predstavlja listu tehnologija nego portfolio.

Problemi:

nema featured projects sekcije;

nema linkova ka najvažnijim repozitorijumima;

nema hackathon kontribucija;

nema brojki: merged PR-ovi, projekti, internship, tehnologije korišćene u konkretnim sistemima;

nema jasnog “primary focus” dela;

postoji suvišan zatvarajući </b> tag u uvodnom HTML-u;

ikonice zauzimaju dosta prostora, ali ne dokazuju nivo znanja;

ne vidi se razlika između tehnologija koje si ozbiljno koristio i onih koje si samo dotakao.


Show more
Saveti su dobri i skoro svi se brzo rešavaju. Po redosledu isplativosti:

Profilni README je najvažniji, jer ga regruteri prvog vide. Dodaj sekciju Featured projects (Webcrawler, TIAC, mini-shell, go-concurrency-lab, ChessEngine kad ga završiš), jedan red o fokusu („systems programming: OS, networking, C++/Rust/Go“), hackathon-e i praksu. Ikonice svedi na jedan red sa onim što si stvarno koristio. Ovo daje najviše za najmanje truda.
Webcrawler: README koji sam ti ranije napisao već ispravlja link ka PLAN.md. Ako ga još nisi ubacio, ubaci ga ili dodaj PLAN.md u repo. Ostalo traje desetak minuta: root LICENSE (ISC), bolji opis na GitHub-u, topics (web-crawler, nodejs, concurrency, http) i terminal GIF napravljen sa vhs ili asciinema.
cursor-usage-plugin: screenshot status bara, link ka VSIX release-u i LICENSE. WSL detalje prebaci u docs/Installation.md. Pošto je ovo projekat za ličnu upotrebu, ne bih ulagao više od toga.
Mogu odmah da ti napišem novi profilni README i skraćeni README za cursor-usage-plugin, pa da ih samo zalepiš. Da li hoćeš?

Da li bi ti mogao da mi realizujes ovaj profilni README.md za pocetak ?

Važi. Prvo čitam tvoj trenutni profilni README i repoe, pa ti šaljem novu verziju spremnu za lepljenje.

Radim na tome, javljam se kad bude spreman.

Novi profilni README je gotov. Šaljem ti fajl za lepljenje u repo Lazzar19/Lazzar19.

Pre objave proveri nekoliko stvari:

U starom README-u piše "Applied Computer Science", a u novom "Software Engineering". Ostavi naziv smera koji je tačan.
Za TIAC sam napisao "Backend internship". Ako ti se zvanično zvalo drugačije, ispravi.
Opise za mini-shell, go-concurrency-lab i ChessEngine sam izveo iz strukture fajlova jer nemaju README, pa ih doteraj po svom.
Uklonio sam suvišni </b>, a ikonice sam sveo na jedan red.

profile_README
.md

2.8kB




No file chosen

Lingxi's Engineer Bot
Details
Library
Computer
Routines are recurring tasks this Bot runs on a schedule. Ask it in chat to set one up.

Voice chat
Voice

Liora
liora
Speed

1x
1
Language

Auto-detect
auto
<h1 align="center">Hi, I'm Lazar 👋</h1> <p align="center"> 3rd-year <b>Software Engineering</b> student @ <b>Faculty of Technical Sciences, Novi Sad</b><br/> <b>Primary focus:</b> systems programming — operating systems, networking, computer architecture — in C++, Rust and Go. </p> <p align="center"> <a href="https://www.linkedin.com/in/lazar-nikolic-41aab6344/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a> </p>
🔧 Featured projects
Project	What it is	Stack
Webcrawler	Concurrent web crawler with a worker pool. ~194 pages/s with 4 workers (0 ms latency), ~88 pages/s with 16 workers at 50 ms simulated latency (Node 20).	Node.js, JavaScript
TIAC-internship	Product & user management REST API: layered architecture, JWT with refresh-token rotation, RBAC, rate limiting, Redis caching, CI, fully containerized.	C#, ASP.NET Core (.NET 10), EF Core, PostgreSQL/SQLite, Redis, Docker
mini-shell	Unix-like shell with its own parser and tab completion. (in progress)	Rust
go-concurrency-lab	Go server plus benchmarks for experimenting with concurrency patterns.	Go
ChessEngine	Bitboard-based chess engine. (in progress)	C++, CMake
🏆 Hackathons
AI4Society Hackathon — NaŠalter (co-author, team The Merge Conflicts): turns a plain-language question about an administrative procedure in Serbia into the right procedure, documents and counter. Live demo
Cursor Hackathon — FirstContrib: matches newcomers to beginner-friendly repositories and gives a concrete plan for their first pull request.
💼 Experience
TIAC — Backend internship: built a production-style ASP.NET Core REST API (repo).
🚧 Currently building / next
mini htop in C++ — process monitor reading /proc
x86 assembly debugger extension for VS Code
learn-coach — Cursor plugin that keeps students in the loop on architectural decisions
🧰 Tech
Used in real projects: C++ · Rust · Go · C# / .NET · JavaScript / Node.js · TypeScript · Python · PostgreSQL · SQLite · Redis · Docker · Git · GitHub Actions · Linux · CMake
Familiar with: C · React · Next.js

<p align="center"> <img src="https://skillicons.dev/icons?i=cpp,rust,go,cs,nodejs,ts,py,postgres,redis,docker,linux,githubactions&perline=12" /> </p>
