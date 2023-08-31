## NOTE: I couldn't find a way to do this even with the hints so I resorted to the internet and here's what I found. 

- Download the cat.jpg file.
- The file states that <i>"Files can always be changed in a secret way"</i> and so it could mean that the file's binary or the file's metadata should have some clue as to where the flag is.
- One option would be to run `$ strings cat.jpg` which would return all the strings present in the binary of the file. This ended up returning a lot of junk so onto the next option.
- I downloaded a tool called "Exiftool" which would help show me the metadata behind a file.
- Run `$ exiftool cat.jpg` would present me with all the metadata information of the file!
- On checking through the contents, the "License" filed appeared to have a long string which corresponded to "base64".
- To decode this base64 string, we run `$ echo <string> |base64 -d` which would decode the string parameter to its original string which is the flag!