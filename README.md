# color-circle
A canvas with cycling colors, rewritten in Brainfuck

`circle.bf` keeps the position of every arc, turns them on each tick and prints the frame as SVG. `circle.html` runs it every 16 ms and puts the frame on the page.

The page fetches `circle.bf`, so serve the folder and open http://localhost:8000/circle.html:

```sh
python3 -m http.server
```

Any 8-bit Brainfuck interpreter runs `circle.bf` in a terminal too, one frame per input byte:

```sh
printf 'xxx' | bf circle.bf
```
