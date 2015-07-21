dev-test
===

Infoshift developer test.

Guidelines
---

Here are the guidelines for this test.

1. You can use any programming platform (ie. php, python, ruby, node.js, c, bash, etc).
2. Contain the runtime. The checker will not install PHP and Apache on their host machine. Eew! Use tools like docker or vagrant.
3. Ask questions if there are things that are unclear.
4. You're not restricted from using external resources like Google and StackOverflow.
5. Although you're not restricted from using external resources, don't just go copy-and-pasting snippets of code. Take the time to learn it.
6. Document your code. Explain the how and why.

Part 1: Program Input
---

Create a program that reads `team.json`.

There are a couple of ways to accomplish this, here are some examples:
- read the file using the platform's standard file io library.
- create an http server that serves the file and consume the file like an http response.
- streaming inputs: `$ cat team.json | myprogram.py --`.

Part 2: Useful Libraries
---

Now that you've read the file, it's now time to parse the file.

If you check the contents of the file, you'll notice that it's in JSON.
Parse it so you can use them within the program.

- You don't need to make a O(1) state-machine JSONParser library.
- `import json`. Just exhibit that you know how to use re-use libraries.

Part 3: Filtering by location
---

> Functions. :)

In this part, you'll be writing a function that filters the members by location.

Here's an example:

```python
# python
# // team = parse_json(team.json)
filter_by_location(team['members'], "PQ")  # You'll write this funtion.
# [{"name": "blah", "location": "PQ", "age": ..}, ...]  # 
```

- Your function must return the objects/dictionaries/hashes that matches the location. Not print it!

Part 4: Filtering by age range
---

> More arguments...

In this part, like the one in part 3, you'll be writing a function that filters 
the members by age range.

```python
# python
filter_by_age_range(members, age_from, age_to)
```

Part 5: Dynamic Filters
---

> Functions are first-class citizens.

In this part, you'll be writing a filter function that uses functions as arguments. That's more than a hint. :)

- You'll be implementing an all-purpose `filter` function.
- Languages usually have this out-of-the-box. You'll be implementing one here, not use it. >:)
