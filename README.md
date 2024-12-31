**Language_Summarization_Tool**

![image](https://github.com/user-attachments/assets/17c71601-f630-4318-85b6-425709d37750)


The **Text Summarization Tool** is a comprehensive project designed to fine-tune the T5 model for summarizing text. It provides a complete pipeline for training the model on custom datasets and integrates a graphical user interface (GUI) for users to generate summaries effortlessly. This tool combines the power of transformer-based models with an easy-to-use interface to make text summarization accessible.  

This project includes various features to streamline the summarization process. The fine-tuning pipeline prepares the T5 model using custom data and optimizes it for generating concise summaries. A preprocessing step ensures that the input data is clean and tokenized effectively. Additionally, the tool includes a Tkinter-based GUI, making it simple for users to input text and view summaries without technical complexities. The fine-tuned model can also be saved and reused for future applications.  

**Dependencies**

To use this tool, several dependencies are required, including Python 3.7 or higher, the Transformers library, PyTorch, pandas, and scikit-learn. Tkinter, which is included in Python’s standard library, handles the GUI. The dataset used for training must contain two key columns: `article`, which holds the main text, and `highlights`, which stores the corresponding summaries. Proper preprocessing ensures that the dataset is ready for tokenization and model training.  

**Training**

The model training process involves several critical steps. The `article` and `highlights` columns are tokenized using the T5 tokenizer. The training configuration uses the `t5-small` model, with encoder layers frozen to speed up the process. Training is conducted over 10 epochs using PyTorch’s `Trainer`. After training, the fine-tuned model is saved locally in a directory named `./fine_tuned_t5` for later use in inference or deployment.  

**Gui Developement**

A user-friendly GUI allows users to interact with the summarization model. Built with Tkinter, the interface provides a text input box where users can paste the text to be summarized. A "Summarize" button processes the input and generates the summary, which is displayed in another text box. This intuitive design ensures that even users with no technical background can easily use the tool.  

**WorkFlow**

To get started, the fine-tuned model must be saved in the specified directory. Users can then run the GUI script to open the summarization tool. Text can be entered directly into the input box, and the summarization process is initiated with a single click. The tool is efficient and produces concise and accurate summaries within seconds.  

For example, given an input text about machine learning, the model might generate a summary emphasizing its focus on learning from data and making predictions autonomously. This demonstrates the model’s ability to distill key information from detailed content.  
The fine-tuned model can also be exported for deployment in other environments. This feature ensures that the model’s capabilities can be integrated into larger systems or shared with collaborators.  
