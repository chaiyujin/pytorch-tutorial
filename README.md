# Installation
1. First, make sure we can use python3.6 or higher. Enter `python` or `python3` in your command line, the version will be shown at first line.
2. Install pytorch with `pip`:
    - Follow instruction in [pytorch.org](https://pytorch.org/).
    - Choose `pip` for **Package**.
    - Choose `None` for **CUDA**.
    - Choose proper python version for **Language**.
3. Try pytorch in command line.
    - Open a `terminal` on MacOS/Linux or a `powershell` on Windows.
    - Enter `python` or `python3`. Make sure it's same with the version you installed pytorch before.
    - Following code will transform a point (1, 2, 3) to (0, 4, 8) with a matrix.
        ```python
        >>> import torch
        >>> import numpy as np
        >>> point = np.asarray([1, 2, 3, 1], dtype=np.float32)
        >>> matrix = np.asarray([
        ...     [1, 0, 0, -1],
        ...     [0, 2, 0, 0],
        ...     [0, 0, 2, 2],
        ...     [0, 0, 0, 1]
        ... ], dtype=np.float32)
        >>> point = torch.from_numpy(point)
        >>> matrix = torch.from_numpy(matrix)
        >>> torch.matmul(matrix, point)
        tensor([0., 4., 8., 1.])
        ```
