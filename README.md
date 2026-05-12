sky130A.tech文件的精简版
每一次提交的.tech文件跑通magic后生成的rules文件都一致(nom工艺角)

## 修改记录

### 2026-05-12 18:48:42 CST

- 参照原版 `pdks/share/pdk/sky130A/libs.tech/magic/sky130A.tech` 补回 PEX 必需的接触电阻参数：diode contact、MV diode contact、poly resistor contact `xpc`。
- 将电容 corner 从单一 nominal 段拆回 nominal/min/max 三组：`hrlc/lrlc` 使用 minimum capacitance，`hrhc/lrhc` 使用 maximum capacitance。
- 补回 nominal capacitance 中 `*poly active` 到 `nwell,pwell well` 的 `defaultoverlap` 定义。
