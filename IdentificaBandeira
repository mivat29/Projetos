def get_card_brand(card_number):
    number = card_number.replace(" ", "").replace("-", "")

    if not number.isdigit():
        return "Número inválido"

    first_two = int(number[:2])
    first_three = int(number[:3]) if len(number) >= 3 else 0
    first_four = int(number[:4]) if len(number) >= 4 else 0
    first_six = int(number[:6]) if len(number) >= 6 else 0

    if number.startswith("4"):
        return "Visa"
    elif 51 <= first_two <= 55 or 2221 <= first_four <= 2720:
        return "MasterCard"
    elif number.startswith("34") or number.startswith("37"):
        return "American Express"
    elif (number.startswith("6011") or
          622126 <= first_six <= 622925 or
          644 <= int(number[:3]) <= 649 or
          number.startswith("65")):
        return "Discover"
    elif number.startswith("36") or number.startswith("38") or number.startswith("39") or 300 <= first_three <= 305:
        return "Diners Club"
    elif (number.startswith("38") or number.startswith("60")):
        return "Hipercard"
    elif (bin_range := int(number[:6])) and (
        401178 <= bin_range <= 401179 or
        431274 <= bin_range <= 431274 or
        438935 <= bin_range <= 438935 or
        451416 <= bin_range <= 451417 or
        457393 <= bin_range <= 457393 or
        504175 <= bin_range <= 504175 or
        506699 <= bin_range <= 506778 or
        509000 <= bin_range <= 509999 or
        627780 <= bin_range <= 627780 or
        636297 <= bin_range <= 636297 or
        636368 <= bin_range <= 636368
    ):
        return "Elo"
    else:
        return "Bandeira desconhecida"

# Exemplo de uso:
card_number = input("Digite o número do cartão: ")
brand = get_card_brand(card_number)
print(f"Bandeira identificada: {brand}")
