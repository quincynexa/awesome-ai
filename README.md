# Awesome AI

## Skills
- [Superpowers](https://github.com/obra/superpowers)
Superpowers打包了20多个可组合的Skill，覆盖软件开发的完整流程。brainstorming、TDD、代码审查、git提交，每个环节都有对应的Skilll来约束Claude的行为。
```
claude plugin install superpowers
```

- [Planning with Files](https://github.com/OthmanAdi/planning-with-files)
Claude code自带的plan mode 有个让人头疼的问题：规划存在对话上下文里，上下文一压缩就丢了。Planning with Files 把规划、进度和知识都写进markdown文件。Claude开始干活前先创建计划文件，每完成一步就更新进度，遇到有用的信息就记到文件里。
```
claude plugin marketplace add OthmanAdi/planning-with-files
claude plugin install planning-with-files
```

- [Code Review](https://github.com/anthropics/claude-plugins-offical/tree/main/plugins/code-review)
Code Review不是让一个Claude从头到尾看代码，而是启动多个agent并行审查同一个PR。有的看逻辑正确性，有的看安全漏洞，有的看代码风格。每个agent给出的问题都带置信度分数，最后按分数过滤，只保留高置信度的反馈。
```
claude plugin install code-review
```

- [Code Simplifier](https://github.com/anthropics/claude-plugins-offical/tree/main/plugins/code-simplifier)
写代码的时候容易堆逻辑，写完跑通了就不想再碰了，Code Simplifier帮你做哪个“写完在看一遍”的事情。它聚焦最近修改过的代码，检查重复逻辑、多余的中间变量、可以合并的条件分支。不改功能，只做简化。
```
claude plugin install code-simplifier
```

- [Ralph Loop]
通过stop hook拦截Claude的退出，把同一个任务重新喂给它。Claude code有个习惯：做到一半就觉得差不多就停下来说“我已经完成了基础框架，你可以在此基础上继续”。Ralph Loop不让它停，Claude试图退出，hook拦截，检查完成条件，没满足条件就塞回去。循环往复，直到真正做完。
关键技巧：完成条件要写得越具体越好。
更好详细例子可以参考：https://awesomeclaude.ai/ralph-wiggum

- [Skill Creator](https://github.com/anthropics/claude-plugins-offical/tree/main/plugins/skill-creator)
觉得不够？就自己造
```
claude plugin install skill-creator
```



