## Versionshantering vs vanliga filer 

Versionshantering innebär att ögonblick i projektet sparas genom commits i Git. Det gör att jag senare kan gå tillbaka i historiken där varje commit har ett unikt hash-ID och se tidigare versioner av min kod.

I min första commit finns alla tre TODO kvar eftersom git sparade hur koden såg ut vid just det tillfället trots att jag har ändrat den efteråt. 

Vanliga filer sparas genom Ctrl + S men det skapar ingen versionshistorik i Git.

## Arbetsytan, Staging och Commit

git status läser bara av läget just nu och sparar ingenting. git add väljer vad du ska spara, till exempel git add index.html. git commit sparar ändringarna med ett meddelande om vad som har hänt sedan senaste commiten. 

Arbetsytan är själva filen på skrivbordet likt ett ark på ett skrivbord. Med git add väljer du vad som ska läggas i ett kuvert (staging). git commit förseglar sedan valet med en mening i ett kuvert som läggs i en arkivlåda. 

Git protesterar med no changes added to commit eftersom commit enbart läser från staging och aldrig direkt från arbetsfilerna. Hoppar man då över git add finns inga nya ändringar i staging att committa, därav felmeddelande vid en direkt commit.

## Lådan hemma vs Montern på GitHub

Skillnaden mellan mappen på datorn och GitHub handlar om var koden och historiken finns och vem som har tillgång till den. Mappen på datorn är lådan hemma, min privata verkstad. Jag kan ändra, experimentera, staga och committa hur mycket jag vill utan att det syns på GitHub. GitHub är glasmontern likt en monter på ett museum, det är offentlig eller delad yta på internet. Det är här den delas med andra. 
git push är det som bär mina commits från lådan hemma till glasmontern. 

Om meddelandet “everything up-to-date” kommer vid en direkt push beror det på att git push enbart tittar på commits, inte på arbetsfilerna. 
