# Install_libIEC61850
How to install pylibIEC61850 in raspberry pi 4, this tutorial based on [Jens Nielsen](https://www.icsrange.com/news/pyiec61850docu-m7dsj?rq=figuring%20out%20the%20libiec61850)

1. Clone the [libIEC61850](https://github.com/mz-automation/libiec61850) version 1.5.1
2. Apply changes to `iec61850.i` with the file in this repo
3. Install the prerequisites: 
   ```bash
   sudo apt-get install build-essential cmake make -y
   ```
4. Navigate to the directory and run:
   ```bash
   sudo cmake -DBUILD_PYTHON_BINDINGS=ON
   ```
5. Then run:
   ```bash
   sudo make
   ```
6. Then run:
   ```bash
   sudo make install
   ```
7. Move `libiec61850.so.1.5.1` from `/usr/local/lib` to `/lib`
8. Try to import the library:
   ```python
   import iec61850
   ```
