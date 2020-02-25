# litex-data-cpu-rocket

Non-Python data files required to use the rocket with
[LiteX](https://github.com/enjoy-digital/litex.git).

The data files can be found under the Python module `litex.data.cpu.rocket`. The
`litex.data.cpu.rocket.location` value can be used to find the files on the file system.
For example;

```python
import litex.data.cpu.rocket

my_data_file = "abc.txt"

with open(os.path.join(litex.data.cpu.rocket.location, my_data_file)) as f:
    print(f.read())
```

The data files come from https://github.com/litex-hub/litex-verilog-rocket
and are imported using `git subtrees` to the directory
[litex/data/cpu/rocket/verilog](litex/data/cpu/rocket/verilog].

## Installing

## Manually

You can install the package manually, however this is **not** recommended.

```
git clone https://github.com/litex-hub/litex-data-cpu-rocket.git
cd litex-data-cpu-rocket
sudo python setup.py install
```

## Using [pip](https://pip.pypa.io/)

You can use [pip](https://pip.pypa.io/) to install the data package directly
from github using;

```
pip install --user git+https://github.com/litex-hub/litex-data-cpu-rocket.git
```

If you want to install for the whole system rather than just the current user,
you need to remove the `--user` argument and run as sudo like so;

```
sudo pip install git+https://github.com/litex-hub/litex-data-cpu-rocket.git
```

You can install a specific revision of the repository using;
```
pip install --user git+https://github.com/litex-hub/litex-data-cpu-rocket.git@<tag>
pip install --user git+https://github.com/litex-hub/litex-data-cpu-rocket.git@<branch>
pip install --user git+https://github.com/litex-hub/litex-data-cpu-rocket.git@<hash>
```

### With `requirements.txt` file

Add to your Python `requirements.txt` file using;
```
-e git+https://github.com/litex-hub/litex-data-cpu-rocket.git
```

To use a specific revision of the repository, use the following;
```
-e https://github.com/litex-hub/litex-data-cpu-rocket.git@<hash>
```