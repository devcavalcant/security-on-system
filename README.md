<h1 align="center">:see_no_evil:Security Tips:hammer:</h1>

## Restrict Sudo

- Use more *sudo* instead *su*
- Lock your *root account*
  - ```
    passwd --lock root
    ```
- If you dont use ssh for login, disable it
  - ```
    [In /etc/ssh/sshd_config]
    
    PermitRootLogin no
    ```
## Kernel

- Restrict Logs
  - ```
    [/etc/sysctl.d/51-dmesg-restrict.conf]

    kernel.dmesg_restrict = 1
    ```
- Disable Kexec
  - ```
    [/etc/sysctl.d/51-kexec-restrict.conf]

    kernel.kexec_loaded_disabled = 1
    ```

    
