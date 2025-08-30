# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 30/08/2025  
Empresa: Abstergo Industries  
Responsável: Thiago José Turibio

---

## Introdução
Este relatório apresenta o processo de implementação de serviços em nuvem na Abstergo Industries, uma distribuidora farmacêutica que atua como hub de integração com diversas farmácias e empresas do setor.  
O objetivo principal é **reduzir custos operacionais** e **aumentar a eficiência** no gerenciamento de estoque, pedidos e comunicação B2B, adotando serviços gerenciados da AWS.

---

## Descrição do Projeto
O projeto foi dividido em 3 etapas, cada uma com foco e ganhos específicos.

### Etapa 1
- **Nome da ferramenta:** Amazon S3  
- **Foco da ferramenta:** Armazenamento de dados seguro, durável e escalável  
- **Descrição de caso de uso:**  
  Armazenar catálogos de produtos, relatórios de estoque, documentos operacionais e integrações (CSV/JSON) com parceiros.  
  Permite versionamento, políticas de acesso e pagamento somente pelo uso, eliminando arquivos em servidores locais.
- **Vantagens (custos):**  
  Sem investimento em storage físico, custo por GB utilizado, redução de manutenção/backup manual.  
- **Ganho principal:**  
  Alta disponibilidade e durabilidade dos dados, acesso rápido e seguro para times internos e parceiros.

### Etapa 2
- **Nome da ferramenta:** Amazon RDS  
- **Foco da ferramenta:** Banco de dados relacional gerenciado.
- **Descrição de caso de uso:**  
  Banco central para pedidos, estoque, notas e integrações com farmácias. Backups automáticos, atualizações gerenciadas e alta disponibilidade.
- **Vantagens (custos):**  
  Reduz custos de administração e de servidores locais; paga-se conforme o tamanho/uso.  
- **Ganho principal:**  
  Confiabilidade e desempenho estável para as operações críticas (pedidos/estoque) com menos esforço de TI.

### Etapa 3
- **Nome da ferramenta:** Amazon EC2  
- **Foco da ferramenta:** Máquinas virtuais escaláveis para aplicações internas  
- **Descrição de caso de uso:**  
  Hospedar o sistema interno de pedidos, APIs B2B e integrações. Possibilidade de escalabilidade conforme picos.
- **Vantagens (custos):**  
  Evita compra de hardware; capacidade sob demanda. Possibilidade de desligar ambientes fora do horário comercial.  
- **Ganho principal:**  
  Flexibilidade para crescer/reduzir recursos rapidamente, mantendo a operação estável.

---

## Conclusão
A adoção de **Amazon S3, Amazon RDS e Amazon EC2** reduz gastos com infraestrutura física e manutenção, ao mesmo tempo em que entrega **escalabilidade, segurança e disponibilidade**. A Abstergo passa a operar com custos previsíveis e proporcionais ao uso, simplificando a gestão de TI e melhorando a integração com parceiros. Com isso, a empresa não só reduz custos, mas também ganha flexibilidade para se adaptar rapidamente às mudanças do mercado farmacêutico.

---

## Anexos

### Comparativo de Custos

| Item                          | Antes (Infra Local) | Depois (AWS)                  |
|-------------------------------|---------------------|-------------------------------|
| Servidores físicos            | R$ 20.000/ano       | R$ 0 (EC2 sob demanda)        |
| Armazenamento de dados        | R$ 10.000/ano       | ~R$ 2.000/ano (S3 pay-per-use)|
| Manutenção de TI (backup, DB) | R$ 15.000/ano       | R$ 5.000/ano (RDS gerenciado) |
| **Total aproximado**          | **R$ 45.000/ano**   | **R$ 7.000/ano**              |

> Observação: valores ilustrativos para evidenciar a redução de custos por uso de serviços gerenciados.

---

Assinatura do Responsável pelo Projeto:  
Thiago José Turibio
