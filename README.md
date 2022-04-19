# GM300 Yükleme

#### Varsayımlar:

* USB Disk'in sürücü harfi
    ```
        X:\
    ```
* Programın daha önce yüklendiği yer:
    ```
        C:\Documents and Settings\User\Desktop\GM300 
    ```

---


### Programı yükleme

1. Windows + R kombinasyonu ile "Çalıştır" penceresi aç.
2. Açılan kutucuğa 'cmd' yaz.

    ```
    cmd
    ```
3. Açılan komut satırında programın daha önce yüklendiği yeri aç
    ```
    cd "C:\Documents and Settings\User\Desktop\GM300"
    ```
4. Bir üst dizine git
    ```
    cd ..
    ```
5. Klasörü zorlayarak sil
    ```
    del GM300 /F
    ```

6. USB Disk'i aç
    ```
    cd X:\
    ```
8. Programı yükle ama çalıştırma 
    ```
    motorola_gm300_xp_software_mr\setup.exe
    ```
7. DLL'yi enjekte et
    ```
    copy MSSTDFMT.DLL C:\WINDOWS
    copy MSSTDFMT.DLL C:\WINDOWS\System32
    regsvr32 C:\WINDOWS\System32\MSSTDFMT.DLL
    ```
9. Bilgisayarı yeniden başlat
    ```
    shutdown -r -t 0
    ```

------
##### Yükleme tamamlandığında başlat menüsünde bir kısayol oluşturulacak.
##### O kısayolu kullanarak programı aç
------
