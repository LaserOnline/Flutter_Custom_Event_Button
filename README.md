
## Flutter Inkwell

### InkWell
```bash
InkWell(
  onTap: () {
    // จะทำงานเมื่อมีการแตะ
  },
  onDoubleTap: () {
    // ทำงานเมื่อมีการแตะสองครั้ง
  },
  onLongPress: () {
    // ทำงานเมื่อกดค้าง
  }
  child: YourWidget(),
)

```
```bash
InkWell(
  onTap: () {
    // จะทำงานเมื่อมีการแตะ
  },
  splashColor: Colors.red, // สีที่แตะ
  highlightColor: Colors.white, // สีที่เน้นเมื่อถูกกด
  child: YourWidget(),
)
```

```bash
InkWell(
  onTap: () {
    // จะทำงานเมื่อมีการแตะ
  },
  customBorder: RoundedRectangleBorder(
    borderRadius: BorderRadius.circular(20.0), // กำหนดรัศมีของสีเมื่อแตะ
  ),
  child: YourWidget(),
)
```


```bash
MouseRegion(
  onEnter: (_) {
    // จะทำงานเมื่อนำเมาส์เข้ามาบนปุ่ม
    setState(() {
      isHovered = true;
    });
  },
  onExit: (_) {
    // จะทำงานเมื่อนำเมาส์ออกจากปุ่ม
    setState(() {
      isHovered = false;
    });
  },
  child: InkWell(
    onTap: () {
      // จะทำงานเมื่อปุ่มถูกแตะ
    },
    splashColor: Colors.blue, // สีที่แตะ
    highlightColor: Colors.white, // สีที่เน้นเมื่อถูกกด
    child: Container(
      decoration: BoxDecoration(
        color: isHovered ? Colors.blue : Colors.transparent, // สีเมื่อ hover
        borderRadius: BorderRadius.circular(20.0),
      ),
      padding: EdgeInsets.all(16.0),
      child: Text("กดที่นี่"),
    ),
  ),
)
```

```bash
InkWell(
  onTap: () {
    // จะทำงานเมื่อมีการแตะ
  },
  splashColor: Colors.red, // สีที่แตะ
  highlightColor: Colors.white, // สีที่เน้นเมื่อถูกกด
  focusColor: Colors.green, // สีเมื่อโฟกัส
  hoverColor: Colors.blue, // สีเมื่อ hover
  borderRadius: BorderRadius.circular(20.0), // กำหนดรัศมีของสีเมื่อแตะ
  customBorder: RoundedRectangleBorder(
    borderRadius: BorderRadius.circular(10.0), // กำหนดรัศมีของสีเมื่อ customBorder ถูกใช้
  ),
  child: YourWidget(),
)
```

---

### GestureDetector
```bash
GestureDetector(
  onTap: () {
    // จะทำงานเมื่อมีการแตะ
  },
  onDoubleTap: () {
    // ทำงานเมื่อมีการแตะสองครั้ง
  },
  onLongPress: () {
    // ทำงานเมื่อกดค้าง
  },
  child: YourWidget(),
)
```

```bash
GestureDetector(
  onTap: () {
    // จะทำงานเมื่อมีการแตะ
  },
  child: Container(
    decoration: BoxDecoration(
      borderRadius: BorderRadius.circular(20.0), // กำหนดรัศมีของสีเมื่อแตะ
      border: Border.all(
        color: Colors.red, // สีที่แตะ
        width: 2.0, // ความกว้างของเส้นขอบ
      ),
    ),
    child: YourWidget(),
  ),
)
```

```bash
bool isHovered = false;

MouseRegion(
  onEnter: (_) {
    setState(() {
      isHovered = true;
    });
  },
  onExit: (_) {
    setState(() {
      isHovered = false;
    });
  },
  child: GestureDetector(
    onTap: () {
      // จะทำงานเมื่อแตะ
    },
    onTapDown: (_) {
      // จะทำงานเมื่อถูกกด
    },
    onTapUp: (_) {
      // จะทำงานเมื่อปล่อยการกด
    },
    child: Container(
      decoration: BoxDecoration(
        color: isHovered ? Colors.blue : Colors.transparent, // สีเมื่อ hover
        borderRadius: BorderRadius.circular(20.0),
      ),
      padding: EdgeInsets.all(16.0),
      child: Text("กดที่นี่"),
    ),
  ),
)
```
