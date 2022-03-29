### vim-easymotion

快速跳转

| 快速跳转                    | Description              |
| --------------------------- | ------------------------ |
| `<leader><leader> s <char>` | Search character         |
| `<leader><leader> f <char>` | Find character forwards  |
| `<leader><leader> F <char>` | Find character backwards |
| `<leader><leader> t <char>` | Til character forwards   |
| `<leader><leader> T <char>` | Til character backwards  |
| `<leader><leader> w`        | Start of word forwards   |
| `<leader><leader> b`        | Start of word backwards  |
| `<leader><leader> e`        | End of word forwards     |
| `<leader><leader> ge`       | End of word backwards    |
| `<leader><leader> j`        | Start of line forwards   |
| `<leader><leader> k`        | Start of line backwards  |

### vim-surround

修改环绕的成对符号

| 修改环绕的成对符号         | Description                                              |
| -------------------------- | -------------------------------------------------------- |
| `y s <motion> <desired>`   | Add `desired` surround around text defined by `<motion>` |
| `d s <existing>`           | Delete `existing` surround                               |
| `c s <existing> <desired>` | Change `existing` surround to `desired`                  |
| `S <desired>`              | Surround when in visual modes (surrounds full selection) |

### CamelCaseMotion

基于驼峰命名的移动

| 基于驼峰命名的移动     | Description                                                                |
| ---------------------- | -------------------------------------------------------------------------- |
| `<leader>w`            | Move forward to the start of the next camelCase or snake_case word segment |
| `<leader>e`            | Move forward to the next end of a camelCase or snake_case word segment     |
| `<leader>b`            | Move back to the prior beginning of a camelCase or snake_case word segment |
| `<operator>i<leader>w` | Select/change/delete/etc. the current camelCase or snake_case word segment |
