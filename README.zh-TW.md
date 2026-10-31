# IfcOpenShell (繁體中文說明)

[Build Status](https://www.google.com/search?q=https://github.com/IfcOpenShell/IfcOpenShell/actions)
[](https://www.gnu.org/licenses/lgpl-3.0)

> 本儲存庫為 [IfcOpenShell/IfcOpenShell](https://github.com/IfcOpenShell/IfcOpenShell) 之個人分叉版本（Fork）。

**IfcOpenShell** 是一套開源的（LGPL 授權）工業基礎類別（Industry Foundation Classes, IFC）軟體庫與開放工具集。它支援開發者與使用者讀取、解析、修改以及轉換 IFC 格式的建築資訊模型（BIM）檔案。

---

## 核心組成模組

1. **IfcOpenShell C++ 核心庫**
   - 基於 Open CASCADE Technology (OCCT) 幾何引擎開發。
   - 提供高效能的 IFC 幾何運算、綱要剖析與拓撲重建。

2. **IfcOpenShell Python (`ifcopenshell`)**
   - 官方 Python 綁定，廣泛應用於自動化腳本、BIM 資料擷取、品質檢驗（QA/QC）與自動化管線。
   - 內建高階 API 模組（`ifcopenshell.api`），以標準工作流程簡化實體建立、屬性集（Pset）指派與幾何賦值。

3. **BIM / BlenderBIM Add-on**
   - 深度整合至 3D 開源建模軟體 Blender 的原生 OpenBIM 編輯插件，支援原汁原味的 IFC 讀寫與參數化編輯。

4. **轉換工具 (`IfcConvert`)**
   - 獨立命令列工具，可將 IFC 檔案快速轉換為 OBJ、DAE、STP、IGS、XML、SVG 或 glTF/GLB 等常見格式。

---

## 快速安裝

### 透過 Python (pip / conda)

最快速取得 Python 函式庫的方式：

```bash
# 使用 pip 安裝預編譯套件
pip install ifcopenshell
```

或使用 Conda：

```bash
conda install -c conda-forge ifcopenshell
```

### 下載命令列工具 (IfcConvert)

預編譯的二進位執行檔（Windows / macOS / Linux）可直接至官方發布頁取得：

- [IfcOpenShell Releases](https://github.com/IfcOpenShell/IfcOpenShell/releases)

---

## Python 快速上手範例

### 1. 讀取 IFC 檔案與查詢元素

```python
import ifcopenshell

# 開啟 IFC 檔案
model = ifcopenshell.open("model.ifc")

# 取得架構版本 (例如 IFC2X3 或 IFC4)
print(f"IFC 綱要版本: {model.schema}")

# 搜尋模型中的所有牆體 (IfcWall)
walls = model.by_type("IfcWall")
print(f"牆體總數: {len(walls)}")

for wall in walls:
    print(f"名稱: {wall.Name}, 全域唯一識別碼 (GUID): {wall.GlobalId}")
```

### 2. 使用 IfcOpenShell API 建立基礎專案與幾何

```python
import ifcopenshell
import ifcopenshell.api

# 建立空白 IFC4 模型
model = ifcopenshell.api.run("project.create_file", version="IFC4")

# 初始化專案與基本度量單位
project = ifcopenshell.api.run("root.create_entity", model, ifc_class="IfcProject", name="My Project")
ifcopenshell.api.run("unit.assign_unit", model, length={"is_metric": True, "raw": "MILLIMETERS"})

# 儲存檔案
model.write("output.ifc")
```

---

## 本地建置與編譯 (Build from Source)

IfcOpenShell 依賴 CMake 與多個第三方庫（如 Open CASCADE、Boost、HDF5、Eigen 等）。推薦使用官方提供的自動化建置腳本：

```bash
# 複製專案
git clone https://github.com/chydesignstudio-Henry/IfcOpenShell.git
cd IfcOpenShell

# 執行自動化建置腳本 (以 Linux / macOS 為例)
cd cmake
python3 build-all.py
```

*詳細建置參數與 Windows Visual Studio 支援說明請參閱 `cmake/` 目錄下之官方指南。*

---

## 相關連結與資源

- **官方首頁**：[ifcopenshell.org](https://ifcopenshell.org/)
- **官方文檔**：[docs.ifcopenshell.org](https://docs.ifcopenshell.org/)
- **社群討論區 / OSArch**：[community.osarch.org](https://community.osarch.org/)
- **上游主儲存庫**：[IfcOpenShell/IfcOpenShell](https://github.com/IfcOpenShell/IfcOpenShell)

---

## 授權條款

IfcOpenShell 採用 **GNU Lesser General Public License (LGPL) v3.0** 授權條款，完整條款請見儲存庫內的 LICENSE 檔案。
