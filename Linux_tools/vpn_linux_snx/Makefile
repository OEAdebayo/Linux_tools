# Makefile for installing snx on Linux

URL=https://netsec.univaq.it/fileadmin/user_upload/Netsec/Download/Immagini/Rete_ateneo/MigrazioneFW/snx_install_linux30.zip
ZIP=snx_install_linux30.zip
SCRIPT=snx_install_linux30.sh

.PHONY: all download unzip chmod install clean

all: install

download:
	wget $(URL) -O $(ZIP)

unzip: $(ZIP)
	unzip -o $(ZIP)

chmod: $(SCRIPT)
	chmod +x $(SCRIPT)

install: download unzip chmod
	sudo ./$(SCRIPT)

clean:
	rm -f $(ZIP)
	rm -f $(SCRIPT)
