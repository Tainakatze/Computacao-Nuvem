# 📂 **Benefícios da Computação em Nuvem**  

## 📝 **Descrição:**  
A computação em nuvem oferece diversas vantagens, possibilitando maior eficiência e flexibilidade para empresas e desenvolvedores. Este programa permite ao usuário explorar os principais benefícios e entender suas características.  

### 📥 **Entrada**  
O usuário pode escolher um dos seguintes benefícios:  
- **Escalabilidade**  
- **Alta Disponibilidade**  
- **Custo sob demanda**  
- **Acesso global**  

Caso o usuário forneça uma entrada inválida, o programa solicitará uma nova tentativa.  

### 📤 **Saída**  
A saída do programa será a descrição correspondente ao benefício informado.  

| **Benefício**             | **Descrição**                           |
|--------------------------|----------------------------------------|
| Escalabilidade          | Cresce ou reduz conforme necessidade  |
| Alta Disponibilidade    | Disponível quase sempre              |
| Custo sob demanda      | Paga apenas pelo que usar            |
| Acesso global          | Acesso de qualquer lugar             |

---

## 🖥️ **Código:**  


```python
def descrever_beneficio(beneficio):
    """ Associa um benefício à sua respectiva descrição """
    beneficios = {
        "Escalabilidade": "Cresce ou reduz conforme necessidade",
        "Alta Disponibilidade": "Disponível quase sempre",
        "Custo sob demanda": "Paga apenas pelo que usar",
        "Acesso global": "Acesso de qualquer lugar"
    }
    return beneficios.get(beneficio, None)

def obter_entrada():
    """ Solicita uma entrada válida do usuário """
    while True:
        print("\nEscolha um benefício da computação em nuvem:")
        print("1. Escalabilidade\n2. Alta Disponibilidade\n3. Custo sob demanda\n4. Acesso global")
        entrada = input("Informe o nome do benefício: ").strip()
        descricao = descrever_beneficio(entrada)
        if descricao:
            return entrada, descricao
        else:
            print("Benefício não reconhecido. Tente novamente.\n")

# Execução do programa
entrada, descricao = obter_entrada()
print(f"\nBenefício escolhido: {entrada}\nDescrição: {descricao}")
```

---

## 🧪 **Testes Automatizados:**  

Para garantir a funcionalidade, foram adicionados testes usando `unittest`:  

```python
import unittest
from programa import descrever_beneficio

class TestBeneficiosNuvem(unittest.TestCase):
    def test_beneficios_validos(self):
        self.assertEqual(descrever_beneficio("Escalabilidade"), "Cresce ou reduz conforme necessidade")
        self.assertEqual(descrever_beneficio("Alta Disponibilidade"), "Disponível quase sempre")
        self.assertEqual(descrever_beneficio("Custo sob demanda"), "Paga apenas pelo que usar")
        self.assertEqual(descrever_beneficio("Acesso global"), "Acesso de qualquer lugar")

    def test_beneficio_invalido(self):
        self.assertIsNone(descrever_beneficio("Benefício inexistente"))

if __name__ == '__main__':
    unittest.main()
```

---

## 📋 Benefícios e Descrições: 

| **Benefício**             | **Descrição**                           |
|--------------------------|----------------------------------------|
| Escalabilidade          | Cresce ou reduz conforme necessidade  |
| Alta Disponibilidade    | Disponível quase sempre              |
| Custo sob demanda      | Paga apenas pelo que usar            |
| Acesso global          | Acesso de qualquer lugar             |

## 🧪 Testes  
Para rodar os testes automatizados, execute:  
```
python -m unittest testes.py
```

## 🤖 Tecnologias utilizadas  
- **Python 3.x**  
- **unittest** (para testes automatizados)  

## 📜 Licença  
Este projeto está sob a licença MIT.

## ✨ Autor  
Criado por [Tainakatze] – Contribuições são bem-vindas! 😊


## 🔍 **Conclusão:**  
A computação em nuvem proporciona flexibilidade, eficiência e economia para empresas e desenvolvedores.Este projeto pode servir de referência para quem deseja entender melhor os impactos positivos da computação em nuvem. 
