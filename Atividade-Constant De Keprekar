n_input = input("Número informado: ")

if not n_input.isdigit():
    print("Erro: número inválido")
else:
    n = int(n_input)
    
    if n < 0 or n > 9999:
        print("Erro: número inválido")
    else:
        resultado = n
        iteracao = 1
        
        while resultado != 6174:
            d1 = resultado // 1000
            d2 = (resultado // 100) % 10
            d3 = (resultado // 10) % 10
            d4 = resultado % 10
            
            if (d1 == d2 == d3) or (d1 == d2 == d4) or (d1 == d3 == d4) or (d2 == d3 == d4):
                print("Erro: o número possui muitos dígitos repetidos")
                resultado = 6174 
                iteracao = 0 
            else:
                v1 = d1
                v2 = d2
                v3 = d3
                v4 = d4
                
                for i in range(4):
                    if v1 > v2:
                        aux = v1
                        v1 = v2
                        v2 = aux
                    if v2 > v3:
                        aux = v2
                        v2 = v3
                        v3 = aux
                    if v3 > v4:
                        aux = v3
                        v3 = v4
                        v4 = aux
                
                ndc = (v1 * 1000) + (v2 * 100) + (v3 * 10) + v4
                ndd = (v4 * 1000) + (v3 * 100) + (v2 * 10) + v1
                
                resultado = ndd - ndc
                
                print("Iteração", iteracao, ":", ndd, "-", ndc, "=", resultado)
                iteracao = iteracao + 1
        
        if iteracao > 0:
            print("Constante de Kaprekar (6174) atingida em", iteracao - 1, "iterações.")
