```python
from typing import ClassVar

from earth.entity import Human, Lovable
from earth.role import Student
from earth.things.computer import (
    OS,
    Editor,
    Framework,
    Language,
    Linux,
    Windows,
)
from earth.utils.links import GitHub
from earth.world import current_world as world


class MingxuanGame(Human, Lovable):
    age: int = 17
    nickname: ClassVar[set] = {"mx", "mxg", "mg", ...}
    role: Student = Student.SENIOR_HIGH

    tools: "list[OS | Editor]" = [
        Windows._11,
        Linux.WSL.Ubuntu,
        Editor.VSCode,
        Editor.IntellijIdea,
    ]
    skills: list[Language] = [Language.Python]
    learning: "list[Language | Framework]" = [
        Language.C,
        Language.JavaScript,
        Language.CSharp,
        Framework.Vue,
        Language.Go,
    ]

    projects: list[GitHub] = [GitHub("Herta-villa/Herta-villa-SDK")]
    contributed: list[GitHub] = [
        GitHub("KimigaiiWuyi/GenshinUID"),
        GitHub("baiqwerdvd/StarRailUID"),
        GitHub("nonebot/nonebot2"),
    ]


me = MingxuanGame()
world.add_thing(me)
world.execute(me)
```
