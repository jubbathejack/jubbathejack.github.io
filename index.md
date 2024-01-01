
# A blog by Jack Parker (jubbathejack)

Maybe I'll write something for it someday. It would likely be code/IT infrastructure related.
My current interests include:
- Ansible automation. Particuarly about how it may be used within enterprise networks.
- Python. I am self-taught and typically write scripts that make an aspect of my work or life easier.
- Producing metrics. I like to gather metrics from things around me and typically put them in a prometheus database.
- Electronics. I am a big fan of micro-electronics. Though my biggest problem is that I seem to have lots of ideas that don't make it past an idea in my head!

## This is some code that will produce a fibonacci number. It was a small project a few years ago.
The repository with this code can be found [here](https://github.com/jubbathejack/fibonacci_seqence/tree/main).
```python
#!/usr/bin/env python3

x = 0
y = 1
seqNum = 2

rangeTop = input("Please enter how many iterations you want to run: ")
rangeTop = int(rangeTop)

print("0: " + str(x))
print("1: " + str(y))

while seqNum <= rangeTop:
    x = (x + y)
    print(str(seqNum) + ": " + str(x))
    seqNum = (seqNum + 1)
    if seqNum > rangeTop:
        print("Fibonacci sequence complete.")
        exit(0)
    else:
        pass
    y = (y + x)
    print(str(seqNum) + ": " + str(y))
    seqNum = (seqNum + 1)
else:
    print("Fibonacci sequence complete.")
    exit(0)
```
