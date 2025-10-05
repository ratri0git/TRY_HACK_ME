# REGULAR EXPRESSIONS

## Task 2: Character Charsets

1. **Match all of the following characters: c, o, g**  
   **Answer**: `[cog]`

2. **Match all of the following words: cat, fat, hat**  
   **Answer**: `[cfh]at`

3. **Match all of the following words: Cat, cat, Hat, hat**  
   **Answer**: `[CcHh]at`

4. **Match all of the following filenames: File1, File2, file3, file4, file5, File7, file9**  
   **Answer**: `[Ff]ile[1-9]`

5. **Match all of the filenames of question 4, except "File7" (use the hat symbol)**  
   **Answer**: `[Ff]ile[^7]`

## Task 3: Wildcards and Optional Characters

1. **Match all of the following words: Cat, fat, hat, rat**  
   **Answer**: `.at`

2. **Match all of the following words: Cat, cats**  
   **Answer**: `[Cc]ats?`

3. **Match the following domain name: cat.xyz**  
   **Answer**: `cat\.xyz`

4. **Match all of the following domain names: cat.xyz, cats.xyz, hats.xyz**  
   **Answer**: `[ch]ats?\.xyz`

5. **Match every 4-letter string that doesn't end in any letter from n to z**  
   **Answer**: `...[^n-z]`

6. **Match bat, bats, hat, hats, but not rat or rats (use the hat symbol)**  
   **Answer**: `[^r]ats?`

## Task 4: Metacharactors and Repetitions

1. **Match the following word: catssss**  
   **Answer**: `cats{4}`

2. **Match all of the following words (use the * sign): Cat, cats, catsss**  
   **Answer**: `[Cc]ats*`

3. **Match all of the following sentences (use the + sign): regex go br, regex go brrrrrr**  
   **Answer**: `regex go br+`

4. **Match all of the following filenames: ab0001, bb0000, abc1000, cba0110, c0000 (don't use a metacharacter)**  
   **Answer**: `[abc]{1,3}[01]{4}`

5. **Match all of the following filenames: File01, File2, file12, File20, File99**  
   **Answer**: `[Ff]ile\d{1,2}`

6. **Match all of the following folder names: kali tools, kali     tools**  
   **Answer**: `kali\s+tools`

7. **Match all of the following filenames: notes~, stuff@, gtfob#, lmaoo!**  
   **Answer**: `\w{5}\W`

8. **Match the string in quotes (use the * sign and the \s, \S metacharacters): "2f0h@f0j0%!     a)K!F49h!FFOK"**  
   **Answer**: `\S*\s*\S*`

9. **Match every 9-character string (with letters, numbers, and symbols) that doesn't end in a "!" sign**  
   **Answer**: `\S{8}[^!]`

10. **Match all of these filenames (use the + symbol): .bash_rc, .unnecessarily_long_filename, and note1**  
    **Answer**: `\.?\w+`

## Task 5: Starts with/ ends with, groups, and either/ or

1. **Match every string that starts with "Password:" followed by any 10 characters excluding "0", irrespective of the position**  
    **Answer**: `Password:[^0]{10}`

2. **Match "username: " in the beginning of a line (note the space!)**  
    **Answer**: `^username:\s`

3. **Match every line that doesn't start with a digit (use a metacharacter)**  
    **Answer**: `^\D`

4. **Match this string at the end of a line: EOF$**  
    **Answer**: `EOF\$`

5. **Match all of the following sentences: I use nano, I use vim**  
    **Answer**: `I use (nano|vim)`

6. **Match all lines that start with $, followed by any single digit, followed by $, followed by one or more non-whitespace characters**  
    **Answer**: `\$\d\$\S+`

7. **Match every possible IPv4 IP address (use metacharacters and groups)**  
    **Answer**: `(\d{1,3}\.){3}\d{1,3}`

8. **Match all of these emails while also adding the username and the domain name (not the TLD) in separate groups (use \w): hello@tryhackme.com, username@domain.com, dummy_email@xyz.com**  
    **Answer**: `(\w+)@(\w+)\.com`
