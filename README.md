# Brave-record
¿Why 001? We need to try to understand, even just a little.

![buh](https://github.com/nicolasbaez/Brave-record/blob/main/why001.png)
```javascript
setup = (_) => {
  createCanvas((w = 500), w);
  r = w / 50;
  l = [];
  for (i = 0; i <= w; i += r) {
    l[i] = [];
    for (j = 0; j <= w; j += r) {
      l[i][j] = int(random(4));
    }
  }
};
lab = (x, y, t, r) => {
  switch (t) {
    case 0:
      line(x, y, x + r, y);
      break;
    case 1:
      line(x, y, x, y + r);
      break;
    case 2:
      line(x, y + r, x + r, y + r);
      break;
    case 3:
      line(x + r, y, x + r, y + r);
      break;
  }
};
draw = (_) => {
  background(255);
  for (i = 0; i <= w; i += r) {
    for (j = 0; j <= w; j += r) {
      lab(i, j, l[i][j], r);
    }
  }
};
