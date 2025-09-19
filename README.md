# 🧠TrendStory: Trending Topic Script Generator

TrendStory is an intelligent NLP pipeline that extracts current trending topics (from platforms like YouTube, or Google) and turns them into themed story scripts (e.g., comedy, sarcasm, tragedy) using the T5 transformer model and a Gradio interface.
    
---

## 📦 Setup    
          
### Prerequisites

Ensure you have Python 3.8+ and the following dependencies installed:

```bash
pip install transformers torch gradio flask-ngrok emoji grpcio grpcio-tools selenium
```

To compile gRPC files (if using gRPC server):

```bash
python -m grpc_tools.protoc -I. --python_out=. --grpc_python_out=. story_service.proto
```

---

## 🚀 Usage

You can run the main service via:

```bash
python <hussain>.ipynb
```

Or use Jupyter Notebook and step through the code interactively.

### Gradio Interface

Once running, access the model interface through the local or public Gradio link. It allows users to input text and receive model-generated output.

---

## 🧰 Architecture

- **Model**: T5 (`t5-large` by default) using Hugging Face `transformers`
- **Frontend**: Gradio Web UI
- **Backend**: Flask server (optional Flask-Ngrok for tunneling)
- **Optional**:
  - gRPC service for remote calls via `.proto` definitions
  - Selenium support for automated browser actions (e.g., content scraping)
  - Emoji preprocessing and cleaning
  - Asynchronous concurrency with `ThreadPoolExecutor` and `asyncio`

---

## 📚 Model Sources

- **Transformer Model**: [`t5-large`](https://huggingface.co/t5-small)
- Tokenizer and model are both loaded from Hugging Face.

---

## ⚠️ Limitations

- gRPC `.proto` files must be compiled manually (`story_service.proto` not bundled here).
- Selenium usage depends on the environment (e.g., ChromeDriver must be correctly configured).
- Not production-hardened—meant for demos and experiments.
- Error handling and security features are minimal.

---

## 📄 License

This project is for educational purposes. Please verify model licenses if used in production.
      
