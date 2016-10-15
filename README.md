# msh
A convenient shell menu, the view and the function are seperated. The view is in msh.etc file, and the function is in msh.fun file. What's showing in the menu is easy to change by only modifying the msh.etc file.


只需要通过简单的配置就可以生成一个shell菜单，包含的功能有：

1. 指定菜单是否必须执行，菜单的后面会显示一个 *
2. 显示菜单执行的结果，成功的会显示一个✓，失败的会显示一个✕
3. 指定当前菜单所依赖的其它菜单，只有依赖的菜单执行成功后，才会允许执行当前菜单
4. 菜单具有层级，一个菜单下可以包含子菜单
