# Objectives

Ascii-art is a program which consists in receiving a `string` as an argument and outputting the `string` in a graphic representation using ASCII. Time to write big.

What we mean by a graphic representation using ASCII, is to write the `string` received using ASCII characters, as you can see in the example below:
```
@@@@@@BB@@@@``^^``^^``@@BB$$@@BB$$
@@%%$$$$^^^^WW&&8888&&^^""BBBB@@@@
@@@@@@""WW8888&&WW888888WW``@@@@$$
BB$$``&&&&WWWW8888&&&&8888&&``@@@@
$$``&&WW88&&88&&&&8888&&88WW88``$$
@@""&&&&&&&&88888888&&&&&&88&&``$$
``````^^``^^^^^^````""^^``^^``^^``
""WW^^@@@@^^``````^^BB@@^^``^^&&``
^^&&^^@@````^^``&&``@@````^^^^&&``
``WW&&^^""``^^WW&&&&""``^^^^&&88``
^^8888&&&&&&WW88&&88WW&&&&88&&WW``
@@``&&88888888WW&&WW88&&88WW88^^$$
@@""88&&&&&&&&888888&&``^^&&88``$$
@@@@^^&&&&&&""``^^^^^^8888&&^^@@@@
@@@@@@^^888888&&88&&&&MM88^^BB$$$$
@@@@@@BB````&&&&&&&&88""``BB@@BB$$
$$@@$$$$$$$$``````````@@$$@@$$$$$$
```
+ This project should handle an input with numbers, letters, spaces, special characters and `\n`.
  
+ Take a look at the ASCII manual.

## Instructions

+ Your project must be written in **Go**.

+ The code must respect the good [practices](https://01.kood.tech/git/root/public/src/branch/master/subjects/good-practices/README.md).

It is recommended to have **test files** for [unit testing](https://go.dev/doc/tutorial/add-a-test).

+ Some **banner** files with a specific graphical template representation using ASCII will be given. The files are formatted in a way that is not necessary to change them.

  + [shadow](https://01.kood.tech/git/root/public/src/branch/master/subjects/ascii-art/shadow.txt)
  + [standard](https://01.kood.tech/git/root/public/src/branch/master/subjects/ascii-art/standard.txt)
  + [thinkertoy](https://01.kood.tech/git/root/public/src/branch/master/subjects/ascii-art/thinkertoy.txt)

## Banner Format

+ Each character has a height of 8 lines.
+ Characters are separated by a new line `\n`.
+ Here is an example of ' ', '!' and '"'(one dot represents one space) :
```
......
......
......
......
......
......
......
......

._..
|.|.
|.|.
|.|.
|_|.
(_).
....
....

._._..
(.|.).
.V.V..
......
......
......
......
......
```

## Usage

```
student$ go run . "" | cat -e
student$ go run . "\n" | cat -e
$
student$ go run . "Hello\n" | cat -e
 _    _          _   _          $
| |  | |        | | | |         $
| |__| |   ___  | | | |   ___   $
|  __  |  / _ \ | | | |  / _ \  $
| |  | | |  __/ | | | | | (_) | $
|_|  |_|  \___| |_| |_|  \___/  $
                                $
                                $
$
student$ go run . "hello" | cat -e
 _              _   _          $
| |            | | | |         $
| |__     ___  | | | |   ___   $
|  _ \   / _ \ | | | |  / _ \  $
| | | | |  __/ | | | | | (_) | $
|_| |_|  \___| |_| |_|  \___/  $
                               $
                               $
student$ go run . "HeLlO" | cat -e
 _    _          _        _    ____   $
| |  | |        | |      | |  / __ \  $
| |__| |   ___  | |      | | | |  | | $
|  __  |  / _ \ | |      | | | |  | | $
| |  | | |  __/ | |____  | | | |__| | $
|_|  |_|  \___| |______| |_|  \____/  $
                                      $
                                      $
student$ go run . "Hello There" | cat -e
 _    _           _    _                 _______   _                              $
| |  | |         | |  | |               |__   __| | |                             $
| |__| |   ___   | |  | |    ___           | |    | |__      ___    _ __     ___  $
|  __  |  / _ \  | |  | |   / _ \          | |    |  _ \    / _ \  | '__|   / _ \ $
| |  | | |  __/  | |  | |  | (_) |         | |    | | | |  |  __/  | |     |  __/ $
|_|  |_|  \___|  |_|  |_|   \___/          |_|    |_| |_|   \___|  |_|      \___| $
                                                                                  $
                                                                                  $
student$ go run . "1Hello 2There" | cat -e
     _    _           _    _                       _______   _                              $
 _  | |  | |         | |  | |               ____  |__   __| | |                             $
/ | | |__| |   ___   | |  | |    ___       |___ \    | |    | |__      ___    _ __     ___  $
| | |  __  |  / _ \  | |  | |   / _ \        __) |   | |    |  _ \    / _ \  | '__|   / _ \ $
| | | |  | | |  __/  | |  | |  | (_) |      / __/    | |    | | | |  |  __/  | |     |  __/ $
|_| |_|  |_|  \___|  |_|  |_|   \___/      |_____|   |_|    |_| |_|   \___|  |_|      \___| $
                                                                                            $
                                                                                            $
student$ go run . "{Hello There}" | cat -e
   __   _    _           _    _                 _______   _                              __    $
  / /  | |  | |         | |  | |               |__   __| | |                             \ \   $
 | |   | |__| |   ___   | |  | |    ___           | |    | |__      ___    _ __     ___   | |  $
/ /    |  __  |  / _ \  | |  | |   / _ \          | |    |  _ \    / _ \  | '__|   / _ \   \ \ $
\ \    | |  | | |  __/  | |  | |  | (_) |         | |    | | | |  |  __/  | |     |  __/   / / $
 | |   |_|  |_|  \___|  |_|  |_|   \___/          |_|    |_| |_|   \___|  |_|      \___|  | |  $
  \_\                                                                                    /_/   $
                                                                                               $
student$ go run . "Hello\nThere" | cat -e
 _    _           _    _           $
| |  | |         | |  | |          $
| |__| |   ___   | |  | |    ___   $
|  __  |  / _ \  | |  | |   / _ \  $
| |  | | |  __/  | |  | |  | (_) | $
|_|  |_|  \___|  |_|  |_|   \___/  $
                                   $
                                   $
 _______   _                              $
|__   __| | |                             $
   | |    | |__      ___    _ __     ___  $
   | |    |  _ \    / _ \  | '__|   / _ \ $
   | |    | | | |  |  __/  | |     |  __/ $
   |_|    |_| |_|   \___|  |_|      \___| $
                                          $
                                          $
student$ go run . "Hello\n\nThere" | cat -e
 _    _           _    _           $
| |  | |         | |  | |          $
| |__| |   ___   | |  | |    ___   $
|  __  |  / _ \  | |  | |   / _ \  $
| |  | | |  __/  | |  | |  | (_) | $
|_|  |_|  \___|  |_|  |_|   \___/  $
                                   $
                                   $
$
 _______   _                              $
|__   __| | |                             $
   | |    | |__      ___    _ __     ___  $
   | |    |  _ \    / _ \  | '__|   / _ \ $
   | |    | | | |  |  __/  | |     |  __/ $
   |_|    |_| |_|   \___|  |_|      \___| $
                                          $
                                          $
student$ go run . "Hello" "shadow" | cat -e
                                 $
_|    _|          _| _|          $
_|    _|   _|_|   _| _|   _|_|   $
_|_|_|_| _|_|_|_| _| _| _|    _| $
_|    _| _|       _| _| _|    _| $
_|    _|   _|_|_| _| _|   _|_|   $
                                 $
                                 $
student$ go run . "Hello" "thinkertoy" | cat -e
                 $
o  o     o o     $
|  |     | |     $
O--O o-o | | o-o $
|  | |-' | | | | $
o  o o-o o o o-o $
                 $
                 $
student$ go run . "Hello" "shadow.txt" | cat -e
                                 $
_|    _|          _| _|          $
_|    _|   _|_|   _| _|   _|_|   $
_|_|_|_| _|_|_|_| _| _| _|    _| $
_|    _| _|       _| _| _|    _| $
_|    _|   _|_|_| _| _|   _|_|   $
                                 $
                                 $  
student$               
```

## Allowed packages

+ Only the [standard Go](https://pkg.go.dev/std) packages are allowed
This project will help you learn about :

+ The Go file system(**fs**) API
+ Data manipulation

## Testing

Make `test.sh` file executable 
```
chmod +x test.sh
```
Run `test.sh` file for tests
```
./test.sh
```

## Error handling with different input files: [LF vs CRLF](https://stackoverflow.com/questions/1552749/difference-between-cr-lf-lf-and-cr-line-break-types)

 `standard.txt` and `shadow.txt` work nicely but you may (or may not) face an error out of range error with `thinkertoy.txt`. `standard.txt` and `shadow.txt` from the original source are `LF` and `thinkertoy.txt` is `CRLF`. 

The Carriage Return (CR) character `(0x0D, \r)` moves the cursor to the beginning of the line without advancing to the next line. This character is used as a new line character in Commodore and Early Macintosh operating systems (OS-9 and earlier).

The Line Feed (LF) character `(0x0A, \n)` moves the cursor down to the next line without returning to the beginning of the line. This character is used as a new line character in UNIX based systems (Linux, Mac OSX, etc)

The End of Line (EOL) sequence `(0x0D 0x0A, \r\n)` is actually two ASCII characters, a combination of the CR and LF characters. It moves the cursor both down to the next line and to the beginning of that line. This character is used as a new line character in most other non-Unix operating systems including Microsoft Windows, Symbian OS and others.

To make it work just format `thinkertoy.txt` as `LF` by clicking to `CRLF` and selecting `LF` as on image below

![LF to CRLF](/img/CRLF-to-LF.png)