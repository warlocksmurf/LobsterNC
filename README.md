# LobsterNC 🦞🐱
Ever get sick of connecting to a CTF server over and over just to input answers one by one, getting kicked out every time you mess up or finish a question? Yeah, me too. LobsterNC automates the whole painful process — it connects once, fires all your answers in sequence like a machine gun, and then hands you the shell to grab your flag without breaking a sweat. No more reconnecting.

## Features
- Connects automatically to a given IP and port.
- Sends a sequence of predefined answers to prompts.
- Drops into an interactive session once all answers are submitted (to grab the flag or continue).
- Lightweight and easy to use.

## Requirements
- Python 3.x
- pwntools

## Usage
1. Clone this repository or download the script.
2. Run the script:
```
python3 lobsternc.py
```
3. When prompted, enter the target IP and port in the format:
```
IP:PORT
```
For example:
```
127.0.0.1:1337
```
4. Enter the answers, separated by commas:
```
answer1, answer2, answer3
```
5. The script will automatically send each answer after receiving each prompt, then give you a live interactive shell to continue.

## Example
```
$ python3 lobsternc.py
Enter target IP and port (format: IP:PORT): 127.0.0.1:9001
Enter answers separated by commas: 42,hello world,password123
[*] Opening connection to 127.0.0.1 on port 9001: Done
```

## Disclaimer
- Make sure the answers are in the correct order as expected by the challenge.
- If the server expects any other type of interaction between answers, you might need to extend the script slightly.
