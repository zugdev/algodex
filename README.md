### an algo collection

*might* add notes and references later

- bfs

- dfs

### understanding

you should know at least the principal structs, for a list of useful util functions dive into `/headers` specially `graph.h`

```c
typedef enum { WHITE, GRAY, BLACK } Color;

typedef struct Node {
  char name;
  int id;
  int distance;
  int t_entering;
  int t_leaving;
  Color color;
  struct Node** neighbors;
  int out_degree;
  struct Node* parent;
} Node;

typedef struct Graph {
  Node** nodes;
  int size;
} Graph;
```

im aggregating all algo properties in a single type struct for commodity I know this is not max efficiency. I think general code is pretty easy to understand, prioritizing clear code x efficiency driven. btw some of those are my thoughts so stuff might not *always* be optimal complexity

### executing

you must have a compiler installed. `Makefile` is set to run `gcc`:

1. if you have a different compiler go into `Makefile` and change the alias
2. if you don't have a compiler installed please refer to [this manual.](https://gcc.gnu.org/install/)

to compile just run:
```shell
make
```

check your `/out` dir and run executables:
```shell
# linux
./out/bfs
```

### commit msg conventions:

- **feat:** for new implementations, code updates, anything meaningfull

example -> feat: implement btp

- **chore:** update comments, settings, .gitignore, dir structure

example -> chore: delete trash code

