def celsius_para_fahrenheit(celsius):
    """Converte Celsius para Fahrenheit"""
    return celsius * 9/5 + 32

def celsius_para_kelvin(celsius):
    """Converte Celsius para Kelvin"""
    return celsius + 273.15



def celsius_para_fahrenheit(celsius):
    return celsius * 9/5 + 32

def celsius_para_kelvin(celsius):
    return celsius + 273.15

def fahrenheit_para_celsius(fahrenheit):
    return (fahrenheit - 32) * 5/9

def fahrenheit_para_kelvin(fahrenheit):
    return (fahrenheit - 32) * 5/9 + 273.15

def kelvin_para_celsius(kelvin):
    return kelvin - 273.15

def kelvin_para_fahrenheit(kelvin):
    return (kelvin - 273.15) * 9/5 + 32

# -menu
def exibir_menu():
    print("\n" + "=" * 45)
    print("           CONVERSOR DE TEMPERATURA")
    print("=" * 45)
    print("1 - Celsius para Fahrenheit")
    print("2 - Celsius para Kelvin")
    print("3 - Fahrenheit para Celsius")
    print("4 - Fahrenheit para Kelvin")
    print("5 - Kelvin para Celsius")
    print("6 - Kelvin para Fahrenheit")
    print("0 - Sair")
    print("=" * 45)

# --- Funções
def main():
    while True:
        exibir_menu()
        opcao = input("Escolha uma opção (0-6): ").strip()

        # Validação da opção de encerramento
        if opcao == '0':
            print("\nEncerrando o conversor de temperatura. Até logo!")
            break

        # Validação das opções válidas do menu
        if opcao in ['1', '2', '3', '4', '5', '6']:
            # Validação da entrada numérica da temperatura
            try:
                valor = float(input("Digite o valor da temperatura: "))
            except ValueError:
                print("\n[Erro] Entrada inválida! Digite apenas números.")
                continue

            # Execução da conversão correspondente
            if opcao == '1':
                resultado = celsius_para_fahrenheit(valor)
                print(f"\n[Resultado] {valor:.2f}°C equivalem a {resultado:.2f}°F")

            elif opcao == '2':
                resultado = celsius_para_kelvin(valor)
                print(f"\n[Resultado] {valor:.2f}°C equivalem a {resultado:.2f}K")

            elif opcao == '3':
                resultado = fahrenheit_para_celsius(valor)
                print(f"\n[Resultado] {valor:.2f}°F equivalem a {resultado:.2f}°C")

            elif opcao == '4':
                resultado = fahrenheit_para_kelvin(valor)
                print(f"\n[Resultado] {valor:.2f}°F equivalem a {resultado:.2f}K")

            elif opcao == '5':
                resultado = kelvin_para_celsius(valor)
                print(f"\n[Resultado] {valor:.2f}K equivalem a {resultado:.2f}°C")

            elif opcao == '6':
                resultado = kelvin_para_fahrenheit(valor)
                print(f"\n[Resultado] {valor:.2f}K equivalem a {resultado:.2f}°F")
        else:
            print("\n[Erro] Opção inválida! Escolha um número entre 0 e 6.")

if __name__ == "__main__":
    main()# Conversor-de-temperatura
