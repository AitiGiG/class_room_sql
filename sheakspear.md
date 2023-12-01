### task-1

    select plaintext from wordform limit 10;

### task-2

    select plaintext from wordform where wordform ilike 'a%';

### task-3

    select title , genretype from work where genretype = 'p';

### task-4

    select avg(totalparagraphs) from work where genretype = 't';

### task-5
    select title from work where totalwords > (SELECT AVG(totalwords) FROM work);
    
### task-6
    SELECT character.charname, speechcount, work.title FROM character LEFT JOIN character_work ON character.charid = character_work.charid LEFT JOIN work ON character_work.workid = work.workid

### task-7
    SELECT ROUND(AVG(character.speechcount)), work.title FROM character JOIN character_work ON character.charid = character_work.charid JOIN work ON character_work.workid = work.workid WHERE work.title = 'Romeo and Juliet' GROUP BY work.title;

### task-8
    select section , sum(wordcount) as sum from paragraph group by section;

### task-9
    select charname ,  speechcount from character where speechcount >= 15 and speechcount <= 30;

### task-10
    select title, year from work where year > 1600 and year < 1700;

### task-11
    select longtitle from work where longtitle like '%the%';

### task-12
    select distinct section from paragraph;
    
### TASK 13
    select chapter.chapterid , chapter.description , work.title from chapter JOIN work ON work.workid = chapter.workid ; 

### task-14
    select paragraph.paragraphnum , character.charname , character.speechcount from paragraph JOIN character ON character.charid= paragraph.charid ;

###  task-15
    select paragraph.paragraphnum , work.title , work.year from paragraph JOIN work ON work.workid= paragraph.workid 