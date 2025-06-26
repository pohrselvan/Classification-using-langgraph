# Classification-using-langgraph

For this Project, I have built a **text classification** system using **BERT** embedded in an **LangGraph**-based pipeline. It can be configured to be robust and self-healing and can give accurate predictions and deal with uncertainty carefully.

The key points are:

- **Transformer-based Classifier:** A fine tunned BERT model handles the core classification task.

- **The LangGraph Workflow:** Transitions between nodes such as inference, confidence tests, and fallbacks are performed using LangGraph, and decision flows are run using LangGraph.

- **Fallback Strategy:**

  - **Human-in-the-loop fallback:** In the event that confidence is low from the model, it will seek user clarification to avoid misclassification.

  - **AI-fallback:** Instead of human input, there is an AI-fallback where the pipeline can be switched to an alternate AI that is powered by an **LLaMA 3.2** and locally hosted through an **Ollama** framework.

Such configuration guarantees that the system will constantly strive for correctness either through high-confidence automation of classification or through clarification procedures on uncertainty situations.

# Instruction For Setting Up 

1. Clone the github repo
   
   ```bash
   git clone https://github.com/pohrselvan/Classification-using-langgraph

3. I have provided jupyter notebook for fine tunning the **Bert** model run it before the `langgraph_chatbot.py`
4. Run the langgraph script
   `python3 langgraph_chatbot.py`
