# doopit

Doit tasks as objects who can be referenced by other tasks

Create [doit tasks](https://pydoit.org) whose targets and other properties you can 
reference from other tasks, avoiding duplication of file names.

Also, you can create classes and subclasses of tasks, defining common file naming
or command invocation schemes.

The task creation is one via task creator functions, following the same conventions
like for [creating tasks in a standard doit file](https://pydoit.org/tasks.html). 
However, the resulting tasks have attributes which can be queried. 

```
import doopit

@doopit.Task
def hello_world():
  return dict(
    action = 
