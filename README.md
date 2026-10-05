# Cybersecurity Chatbot Starter

A console chatbot (C#, .NET, Visual Studio 2022) that greets the user by name and answers
basic questions about password safety, phishing and safe browsing.

## How to run
1. Open the .sln file in Visual Studio 2022.
2. Press F5 (or Ctrl+F5).
3. Enter your name, then type a topic, a menu number (1-3), `menu`, or `exit`.

## Why automatic properties?
Automatic properties (BotName, UserName, CurrentTopic) give controlled access to the
object's data with very little code. The compiler creates the backing field, and we can
later add validation without changing the code that uses them. They also replace separate
duplicate variables.

## Why a CyberChatbot class?
Putting the data and behaviour in a class keeps Program.cs short (start and flow only).
Each response is in its own method, so the code is easier to read, test, reuse and extend
than one large block in Program.cs.

## Validation and exception handling
Empty names and queries are rejected so the bot never works with missing data. int.TryParse
checks menu input without crashing on non-numbers, and numbers outside 1-3 give a clear
message. Unknown queries get a helpful reply instead of silence or an error.
