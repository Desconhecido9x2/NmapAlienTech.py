import subprocess

def banner():
    print("""
▗▖  ▗▖▗▞▀▜▌▄▄▄▄  ▄▄▄▄
▐▛▚▖▐▌▝▚▄▟▌█ █ █ █   █
▐▌ ▝▜▌     █   █ █▄▄▄▀
▐▌  ▐▌           █
                 ▀
    [ NMAP Python Tool ]
""")

def nmap_scan(target, full=False):
    if full:
        command = ["nmap", "-Pn", "-p-", target]
    else:
        command = ["nmap", "-Pn", "-F", target]
    print(f"\nScanning {target} ...\n")
    try:
        output = subprocess.check_output(command, un>
        print(output)
    except Exception as e:
        print(f"Erro durante o scan: {e}")

def main():
    while True:
        banner()
        print("1) Scan Nmap Rápido")
        print("2) Scan Nmap Completo (todas portas)")
        print("0) Sair")
        opt = input("Escolha: ")
        if opt == "1":
            target = input("Digite o IP ou domínio: >
            nmap_scan(target)
        elif opt == "2":
            target = input("Digite o IP ou domínio: >
            nmap_scan(target, full=True)
        elif opt == "0":
            print("Saindo...")
            break
        else:
            print("Opção inválida!")
        input("Pressione ENTER para continuar...")
        
if __name__ ==
    main()

