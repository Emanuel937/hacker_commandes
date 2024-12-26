# hacker_commandes
put all command to hack 


## Hydra (Attaque de services en réseau, ex. SSH, FTP, HTTP):

    Installation : sudo apt install hydra
    Commande typique :

    hydra -l admin -P /chemin/liste_mots_passe.txt -t 4 ssh://192.168.1.1

    Description :
        -l : Nom d'utilisateur.
        -P : Chemin du fichier contenant les mots de passe.
        -t : Nombre de threads (pour accélérer).

## Aircrack-ng (Force brute de clés Wi-Fi) :

### Capture du handshake :

    airodump-ng wlan0mon

### Lancer la force brute sur un handshake capturé :

    -aircrack-ng -w /chemin/liste_mots_passe.txt -b [BSSID] fichier_capture.cap

## John the Ripper (Crack de mots de passe hors ligne) :

    Commande typique :

    -john --wordlist=/chemin/liste_mots_passe.txt hash_fichier.txt

Hashcat (Crack de hash avec GPU accélération) :

    Commande typique :

    hashcat -m 2500 -a 0 fichier_hashes.hccapx /chemin/liste_mots_passe.txt
