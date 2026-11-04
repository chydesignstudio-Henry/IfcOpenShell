<!-- This file was generated with the assistance of an AI coding tool. -->

> **翻譯說明：** 這是英文 [README.md](README.md) 的繁體中文（臺灣）翻譯，說明 IfcOpenShell 是什麼、有哪些功能，以及如何安裝與使用。連結、專案名稱與徽章都維持原文，沒有改網址。譯文若與英文不一致，請以英文原文為準。
>
> - 英文原文：[README.md](README.md)
> - 上游儲存庫：[IfcOpenShell/IfcOpenShell](https://github.com/IfcOpenShell/IfcOpenShell)

IfcOpenShell
============

<p align="center">
<img src="https://github.com/IfcOpenShell/IfcOpenShell/assets/88302/34901387-e2dd-4a0c-8e38-9ffc32a66cde">
</p>


IfcOpenShell 是一套開源（[LGPL]）軟體函式庫，用來處理工業基礎類別（Industry Foundation Classes，[IFC]）。[IFC2x3 TC1]、[IFC4 Add2 TC1]、IFC4x1、IFC4x2 與 [IFC4x3 Add2] 都提供完整的解析；幾何方面則完整支援 [IFC2x3 TC1] 與 [IFC4 Add2 TC1]。使用 C++ 時，可以在編譯期擴充任意 IFC schema（綱要）；使用 Python 時，則可以在執行期擴充。

除了 C++ 與 Python API，IfcOpenShell 也附帶一整組工具，其中包含 IfcConvert（將 IFC 模型轉換成其他格式的應用程式）、Bonsai（Blender 附加元件，提供圖形化的 IFC 編寫平台），以及其他函式庫與命令列工具。另外也支援 BCF、IDS 等輔助標準。

若要進一步了解、安裝或開始使用，請看：

* [IfcOpenShell 網站](https://ifcopenshell.org)
* [IfcOpenShell 文件](https://docs.ifcopenshell.org)
  * [IfcOpenShell C++ 安裝](https://docs.ifcopenshell.org/ifcopenshell/installation.html)
  * [IfcOpenShell Python 安裝](https://docs.ifcopenshell.org/ifcopenshell-python/installation.html)
  * [IfcOpenShell Python Hello World 教學](https://docs.ifcopenshell.org/ifcopenshell-python/hello_world.html)
* [Bonsai 網站](https://bonsaibim.org)
* [Bonsai 文件](https://docs.bonsaibim.org/index.html)
  * [附加元件安裝](https://docs.bonsaibim.org/quickstart/installation.html)
  * [瀏覽 IFC 模型](https://docs.bonsaibim.org/quickstart/explore_model.html)

本專案的開發仰賴各位慷慨的捐助！

[![Open Collective Contributors](https://img.shields.io/opencollective/all/opensourcebim?label=Sponsors&color=22ce5f)](https://opencollective.com/opensourcebim/)

內容
----

| 名稱                      | 說明                                                           | 授權             | 服務 |
| ------------------------- | --------------------------------------------------------------------- | ------------------- | ------- |
| [bcf](https://docs.ifcopenshell.org/bcf.html)                       | 讀寫 BCF-XML，並查詢 OpenCDE BCF-API 模組的函式庫   | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/bcf-client?label=PyPI&color=006dad)](https://pypi.org/project/bcf-client/) [![Anaconda-Server Badge](https://anaconda.org/conda-forge/bcf-client/badges/version.svg)](https://anaconda.org/conda-forge/bcf-client) |
| [bonsai](https://docs.ifcopenshell.org/bonsai.html)                    | 在 Blender 提供圖形化、原生 IFC 編寫平台的附加元件 | GPL-3.0-or-later    | [![Official](https://img.shields.io/badge/BonsaiBIM.org-Download-70ba35)](https://bonsaibim.org/studio.html) [![GitHub Unstable](https://img.shields.io/github/v/release/ifcopenshell/ifcopenshell?filter=bonsai-*&label=GitHub-Unstable&color=f6f8fa)](https://github.com/IfcOpenShell/IfcOpenShell/releases?q=bonsai&expanded=true) |
| [bsdd](https://docs.ifcopenshell.org/bsdd.html)                      | 查詢 bSDD API 的函式庫                                         | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/bsdd?label=PyPI&color=006dad)](https://pypi.org/project/bsdd/) |
| [ifc2ca](https://docs.ifcopenshell.org/ifc2ca.html)                    | 把 IFC 結構分析模型轉成 Code_Aster 的工具       | LGPL-3.0-or-later   |
| [ifc4d](https://docs.ifcopenshell.org/ifc4d.html)                     | 在 IFC 與專案管理軟體之間轉換               | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifc4d?label=PyPI&color=006dad)](https://pypi.org/project/ifc4d/) |
| [ifc5d](https://docs.ifcopenshell.org/ifc5d.html)                     | 從 IFC 報告並最佳化成本資訊                         | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifc5d?label=PyPI&color=006dad)](https://pypi.org/project/ifc5d/) |
| ifcblender                | 早期的 Blender IFC 匯入附加元件                                    | LGPL-3.0-or-later\* |
| [ifccityjson](https://docs.ifcopenshell.org/ifccityjson.html)               | 把 CityJSON 轉成 IFC                                               | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifccityjson?label=PyPI&color=006dad)](https://pypi.org/project/ifccityjson/) |
| [ifcclash](https://docs.ifcopenshell.org/ifcclash.html)                  | 碰撞檢查函式庫與命令列工具                                   | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifcclash?label=PyPI&color=006dad)](https://pypi.org/project/ifcclash/) |
| [ifcconvert](https://docs.ifcopenshell.org/ifcconvert.html)                | 把 IFC 轉成多種格式的命令列工具                          | LGPL-3.0-or-later\* | [![Official](https://img.shields.io/badge/IfcOpenShell.org-Download-70ba35)](https://docs.ifcopenshell.org/ifcconvert/installation.html) [![GitHub](https://img.shields.io/github/v/release/ifcopenshell/ifcopenshell?filter=ifcconvert-*&label=GitHub&color=f6f8fa)](https://github.com/IfcOpenShell/IfcOpenShell/releases?q=ifcconvert&expanded=true)
| [ifccsv](https://docs.ifcopenshell.org/ifccsv.html)                    | 從 IFC 匯出與匯入明細表的函式庫與命令列工具           | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifccsv?label=PyPI&color=006dad)](https://pypi.org/project/ifccsv/) |
| [ifcdiff](https://docs.ifcopenshell.org/ifcdiff.html)                   | 比較 IFC 模型之間的變更                                    | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifcdiff?label=PyPI&color=006dad)](https://pypi.org/project/ifcdiff/) |
| [ifcedit](https://docs.ifcopenshell.org/ifcedit.html)                   | 把 ifcopenshell.api 的模型修改函式包成命令列工具         | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifcedit?label=PyPI&color=006dad)](https://pypi.org/project/ifcedit/) |
| [ifcfm](https://docs.ifcopenshell.org/ifcfm.html)                     | 依設施管理（FM）移交需求擷取 IFC 資料                         | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifcfm?label=PyPI&color=006dad)](https://pypi.org/project/ifcfm/) |
| [ifcmax](https://docs.ifcopenshell.org/ifcmax.html)                    | 早期讓 3DS Max 支援 IFC 的擴充功能                         | LGPL-3.0-or-later\* | [![Official](https://img.shields.io/badge/IfcOpenShell.org-Download-70ba35)](https://docs.ifcopenshell.org/ifcmax.html)
| [ifcmcp](https://docs.ifcopenshell.org/ifcmcp.html)                    | 查詢與編輯 IFC 建築模型的 MCP 伺服器               | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifcopenshell-mcp?label=PyPI&color=006dad)](https://pypi.org/project/ifcopenshell-mcp/) |
| [ifcopenshell-python](https://docs.ifcopenshell.org/ifcopenshell-python.html)       | 用來操作 IFC 的 Python 函式庫                                   | LGPL-3.0-or-later\* | [![Official](https://img.shields.io/badge/IfcOpenShell.org-Download-70ba35)](https://docs.ifcopenshell.org/ifcopenshell-python/installation.html) [![GitHub](https://img.shields.io/github/v/release/ifcopenshell/ifcopenshell?filter=ifcopenshell-python-*&label=GitHub&color=f6f8fa)](https://github.com/IfcOpenShell/IfcOpenShell/releases?q=ifcopenshell-python&expanded=true) [![PyPI](https://img.shields.io/pypi/v/ifcopenshell?label=PyPI&color=006dad)](https://pypi.org/project/ifcopenshell/) [![Anaconda](https://img.shields.io/conda/vn/conda-forge/ifcopenshell?label=Anaconda&color=43b02a)](https://anaconda.org/conda-forge/ifcopenshell) [![Anaconda](https://img.shields.io/conda/vn/ifcopenshell/ifcopenshell?label=Anaconda-Unstable&color=43b02a)](https://anaconda.org/ifcopenshell/ifcopenshell) [![Docker](https://img.shields.io/docker/pulls/aecgeeks/ifcopenshell?label=Docker&color=1D63ED)](https://hub.docker.com/r/aecgeeks/ifcopenshell) [![AUR](https://img.shields.io/aur/version/ifcopenshell?label=AUR&color=1793d1)](https://aur.archlinux.org/packages/ifcopenshell) [![AUR Unstable](https://img.shields.io/aur/version/ifcopenshell-git?label=AUR-Unstable&color=1793d1)](https://aur.archlinux.org/packages/ifcopenshell-git) [![Pyodide WASM Wheels tag](https://img.shields.io/github/v/tag/ifcopenshell/wasm-wheels?sort=semver&label=pyodide-wasm-wheels)](https://github.com/IfcOpenShell/wasm-wheels) |
| [ifcpatch](https://docs.ifcopenshell.org/ifcpatch.html)                  | 用來執行現成腳本、修改 IFC 的工具                | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifcpatch?label=PyPI&color=006dad)](https://pypi.org/project/ifcpatch/) |
| [ifcquery](https://docs.ifcopenshell.org/ifcquery.html)                  | 查詢與檢視 IFC 建築模型的命令列工具              | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifcquery?label=PyPI&color=006dad)](https://pypi.org/project/ifcquery/) |
| [ifcsverchok](https://docs.ifcopenshell.org/ifcsverchok.html)               | 用視覺化節點做 IFC 程式設計的 Blender 附加元件                   | GPL-3.0-or-later    | [![GitHub](https://img.shields.io/github/v/release/ifcopenshell/ifcopenshell?filter=ifcsverchok-*.*.*&label=GitHub&color=f6f8fa)](https://github.com/IfcOpenShell/IfcOpenShell/releases?q=ifcsverchok&expanded=true)
| [ifctester](https://docs.ifcopenshell.org/ifctester.html)                 | 以 IDS 審核模型的函式庫、命令列工具與網頁應用                        | LGPL-3.0-or-later   | [![PyPI](https://img.shields.io/pypi/v/ifctester?label=PyPI&color=006dad)](https://pypi.org/project/ifctester/) |

IfcOpenShell 的 C++ 程式碼拆成多個內部函式庫：

| 名稱                      | 說明                                                           | 授權             |
| ------------------------- | --------------------------------------------------------------------- | ------------------- |
| ifcgeom                   | IfcOpenShell 的內部函式庫                                     | LGPL-3.0-or-later\* |
| ifcgeomserver             | IfcOpenShell 的內部函式庫                                     | LGPL-3.0-or-later\* |
| ifcparse                  | IfcOpenShell 的內部函式庫                                     | LGPL-3.0-or-later\* |
| ifcwrap                   | IfcOpenShell 的內部函式庫                                     | LGPL-3.0-or-later\* |
| serializers               | IfcOpenShell 的內部函式庫                                     | LGPL-3.0-or-later\* |

[LGPL]: https://github.com/IfcOpenShell/IfcOpenShell/tree/master/COPYING.LESSER "LGPL-3.0-or-later"
[IFC]: https://technical.buildingsmart.org/standards/ifc/ "IFC"
[IFC2x3 TC1]: https://standards.buildingsmart.org/IFC/RELEASE/IFC2x3/TC1/HTML/ "IFC2x3 TC1"
[IFC4 Add2 TC1]: https://standards.buildingsmart.org/IFC/RELEASE/IFC4/ADD2_TC1/HTML/ "IFC4 Add2 TC1"
[IFC4x3 Add2]: https://standards.buildingsmart.org/IFC/RELEASE/IFC4_3/ "IFC4x3 Add2"
