# python_scripting


## 1) What is Python Scripting?

A script is a small program that automates a task.

Mental model:

Input → Process → Output → Automation

## 2) Running Python Scripts
python script.py

Make executable (Linux/Mac):

#!/usr/bin/env python3
chmod +x script.py
./script.py

## 3) Variables & Data Types
name = "Amith"      # string
age = 25            # int
price = 99.99       # float
is_active = True    # boolean
items = [1,2,3]     # list
user = {"id":1}     # dictionary

## 4) Input & Output
name = input("Enter name: ")
print("Hello", name)

## 5) Conditions
if age > 18:
    print("Adult")
elif age == 18:
    print("Just Adult")
else:
    print("Minor")
    
## 6) Loops
For loop
for i in range(5):
    print(i)
While loop
while True:
    break
    
## 7) Functions
def add(a, b):
    return a + b
    
## 8) File Handling
# Write
with open("data.txt", "w") as f:
    f.write("Hello")

# Read
with open("data.txt") as f:
    content = f.read()
    
## 9) Exception Handling
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Error")
finally:
    print("Done")
    
## 10) Modules & Imports
import math
print(math.sqrt(16))

Install external packages:

pip install requests

## 11) Virtual Environment
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate # Mac/Linux

## 12) Working with JSON
import json

data = {"name":"Amith"}
json_str = json.dumps(data)

obj = json.loads(json_str)

## 13) Command Line Arguments
import sys
print(sys.argv)

Better way:

import argparse

parser = argparse.ArgumentParser()
parser.add_argument("--name")
args = parser.parse_args()
print(args.name)

## 14) OS & Automation
import os

files = os.listdir(".")
print(files)

Run shell command:

import subprocess
subprocess.run(["ls", "-l"])

## 15) Logging
import logging
logging.basicConfig(level=logging.INFO)
logging.info("Started")

## 16) Best Practices

• Use meaningful variable names
• Keep functions small
• Handle errors
• Use logging, not print
• Use virtual environments
• Add comments for complex logic
• Keep secrets in environment variables

## 17) Popular Libraries

Automation → os, shutil, subprocess
APIs → requests
Data → pandas
Dates → datetime
CLI tools → argparse
Paths → pathlib

## 18) Common Real-World Script Uses (DevOps / SRE)

• Log cleanup
• Health checks
• Monitoring scripts
• File converters
• API data fetchers
• Deployment helpers
• Report generators

## 19) Script Structure (Clean Template)
#!/usr/bin/env python3
import logging

def main():
    logging.info("Program started")

if __name__ == "__main__":
    main()
