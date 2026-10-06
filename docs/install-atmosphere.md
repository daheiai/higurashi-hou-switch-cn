# Switch 实机（Atmosphère）安装指南

适用于**已破解的 Nintendo Switch**，通过 Atmosphère 的 LayeredFS 加载补丁，不需要修改游戏本体。

## 前置条件

- 已破解的 Switch，已安装 **Atmosphère 1.12.0 及以上**（并更新 fusee）
- 系统版本 23.0.0 / 23.0.1
- 游戏本体《寒蝉鸣泣之时奉》，Title ID `0100F6A00A684000`
- 游戏版本与补丁匹配：**V2.0 → 2.0.0 / 2.0.2**；**V1.1 → 1.0.0 / 1.2.0**

## 步骤

1. **完全退出游戏。**
2. 解压下载的补丁包，打开 `Atmosphere_SD_真实机复制到SD卡根目录/`。
3. 把里面的 `atmosphere` 文件夹复制到 **SD 卡根目录**，合并目录并覆盖同名文件。
4. 确认补丁文件已就位：
   - `atmosphere/contents/0100F6A00A684000/romfs/patch.rom`
   - `atmosphere/contents/0100F6A00A684000/romfs/patch.rmm`
   - `atmosphere/exefs_patches/higurashi_cn/*.ips`
5. 启动游戏。

## 注意

- `patch.rom` / `patch.rmm` 与 `exefs_patches` 里的 IPS **必须一起安装**：前者提供 ROM2 资源与中文字体，后者负责 CP932 字符映射与界面字符串寻址。只装一半会出现缺字、乱码或界面不生效。
- **不要同时保留**其它路径下的旧汉化或冲突补丁。
- Atmosphère 1.12.0 中，`atmosphere/contents/<TitleID>/` 与 `atmosphere/exefs_patches/` 的路径与加载机制**没有变化**。
- 补丁**不包含存档**，也不会覆盖存档。回退时请使用完整的旧版补丁，避免混用不同版本的文本、字库和 IPS。
