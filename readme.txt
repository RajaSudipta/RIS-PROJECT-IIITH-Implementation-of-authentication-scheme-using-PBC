1. PBC Library installation and setup:

    Step 1: sudo apt-get update

    Step 2: sudo apt-get install m4 flex bison

    Step 3: sudo apt-get install libgmp3-dev

    Step 4: Download pbc library from this link -> https://crypto.stanford.edu/pbc/files/pbc-0.5.14.tar.gz

    Step 5: Create a new Folder somewhere(Desktop) in the name let's say "ris"

    Step 6: Extract the pbc library inside this folder "ris"

    Step 7: Navigate to the ris folder (cd ~/Desktop/ris/pbc-0.5.14/)

    Step 8: ./configure

    Step 9: make

    Step 10: sudo make install

    Step 11: sudo gedit /etc/ld.so.conf.d/newlib.conf

    Step 12: put this in gedit file -> /usr/local/lib and save it

    Step 13: sudo ldconfig

    Step 14: sudo apt-get install libgpg-error-dev
    
2. Extract our codebase zip in the "ris" folder which was created in Desktop

3. Now open 3 terminals from location "~/Desktop/ris" and run these commands

4. Terminal 1(for AP)
    cd AP
    gcc AP.c -o AP -L. -lpbc -lgmp
    ./AP <../a.param

5. Terminal 1(for Client)
    cd Client
    gcc Client.c -o Client -L. -lpbc -lgmp
    ./Client <../a.param

6. Terminal 1(for NM)
    cd NM
    gcc NM.c -o NM -L. -lpbc -lgmp
    ./NM <../a.param
