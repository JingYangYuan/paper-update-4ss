<p align="center">
  <img src="docs/banner.svg" alt="paper-update-4ss" width="100%">
</p>

# Paper 知识更新 4SS（update 模块独立版）

社会科学论文技能包全包候选更新系统。用于从学术专著、教材、期刊论文、综述、课程材料、研究笔记、方法手册和本地经验中生成待人工审核的更新包，可指向 design、lit、outline、analysis、write、submission 与 update 自身。只输出到 paper-workspace/07-update/，不得直接修改任何核心模块文件。

本包由 `paper-master-4ss/scripts/export_standalone.py` 从总控包 `paper-master-4ss/modules/update/` 自动导出：

- 包内相对路径相对本包根目录解析；
- `master/` 与 `references/` 中的协议/治理文件是导出时拷贝的快照；
- 跨模块路径 `paper-master-4ss/modules/<x>/...` 相对同级安装的总控包解析；
- 更新方式：修改总控包对应模块后运行
  `python3 paper-master-4ss/scripts/export_standalone.py update` 重新导出，勿直接编辑本包。

## 它做什么

从专著、教材、论文、课程材料、笔记和方法手册生成**待人工审核**的更新包，可指向 design、lit、outline、analysis、write、submission 与 update 自身。

只写到 `paper-workspace/07-update/`，不得直接修改任何核心模块文件。

## 使用

将本目录安装为宿主 skill（与 `paper-master-4ss` 总控包同级）。入口见 `SKILL.md`。合并进总控包必须经人工确认。
