## NOTE: This cannot be done on mac/windows (or atleast I couldn't)

- Use the WebShell from picoCTF.
- Get the `warm` file saved into the WebShell system using `$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm`.
- Since the file doesn't have executable permissions(check this by running `ls -l warm`) we have to give it the permission.
- We can give it permissions by using `chmod`(learn more by tying `man chmod` into the terminal).
- Type `$ chmod +x warm` (we're adding the executable permission "x" for the file "warm").
- Now run the file using ./warm where you'll see a message indicating us to use '-h' while executing. ("-h" is commonly used with executable files to learn more about the functions of the file.)
- Finally run `./warm -h` to get the flag!