# What is this?

This folder contains some files that can be used to illustrate an example **dyndoc workflow** using Stata.

The dyndoc workflow consists of

- writing markdown/code and
- using Stata to compile the markdown to HTML.

# How should I folllow this example?

First take a look the file called `example-input.txt`. This file contains the markdown/code for the example.

Next, run the Stata script called `dyndoc-command.do`. Note that this Stata "script" contains a single line:

```
dyndoc example-input.txt, replace saving("example-output.html")
```

Here, we are telling Stata to compile the markdown in `example-input.txt` and then save the result as `example-output.html`.

# What can I do with `example-output.html`?

If you take a look at the output file `example-output.html`, you'll see that it is meant to go inside the `<body>` tag of a "real" HTML file:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>

  <!-- PLACE THE CONTENTS OF example-output.html HERE }} -->

</body>
</html>
```

# How can I add styling (CSS) to my output?

- First, put the HTML produced by `dyndoc` inside the body of a "real" HTML file (as mentioned above).
- Then add styling in the `<head>` tag of your HTML file.

For an example of some simple styling, see the file called `example-output-with-css.html`.
