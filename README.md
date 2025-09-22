# Analisador Inteligente de Currículos de TI
Este projeto utiliza Processamento de Linguagem Natural (PLN) para analisar e ranquear currículos de TI. Ele processa um arquivo .zip de currículos em PDF, extrai informações usando RAG (Retrieval-Augmented Generation) e utiliza busca semântica e similaridade do cosseno para pontuar os candidatos com base em habilidades, idiomas e cargo desejados.

### Última versão - Branch: Final. FileName: Projeto_PLN_Avaliacao_Vagas.ipynb

#### Tecnologias Principais: Python, LangChain, Sentence Transformers, Llama 3.1 8bilhões de parâmetros (via Ollama).

### Como Executar no Google Colab

1.  **Configurar o Ambiente no Colab:**
    * **Abra o Notebook:** Faça o upload do arquivo `.ipynb` deste repositório para o [Google Colab](https://colab.research.google.com/).
2.  **Adicionar Currículos:**
    * No menu à esquerda do Colab, clique no ícone de pasta e faça o upload do seu arquivo `curriculos.zip`, com os currículos em PDF que deseja analisar.
3.  **Definir a Vaga:**
    * Na célula de código apropriada, edite o dicionário `input_rh` com as habilidades, idioma e cargo que você está buscando, com cada valor separados por vírgula.
        ```python
        input_rh = {
            'habilidades': 'Java,Spring,Docker,Scrum',
            'idiomas': 'Português,Inglês',
            'cargo': 'Desenvolvedor de Software Sênior'
        }
        ```

4.  **Executar:**
    * No menu do Colab, clique em "Ambiente de execução", depois em "Alterar o tipo de ambiente de execução" e selecione a opção *GPU*, para melhor performance.
    * Clique em *Executar Tudo* para executar todas as células.
O ranking dos melhores currículos, com suas pontuações detalhadas, será exibido no final da execução do notebook.
