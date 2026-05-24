# ch1 — FastAPI Intro

Two FastAPI examples: a static joke endpoint and an LLM-powered joke generator via Groq.

## Setup

```bash
uv sync
```

## Scripts

### 1. Static Jokes (`1_get_joke.py`)

Returns a random hardcoded joke.

```bash
uv run fastapi dev 1_get_joke.py
```

`GET http://localhost:8000/joke`

---

### 2. AI-Generated Jokes (`2_generate_jokes.py`)

Generates a joke on any topic using Groq.

**Configure env:**

```bash
cp .env.sample .env
# fill in GROQ_API_KEY and GROQ_MODEL in .env
```

```bash
uv run fastapi dev 2_generate_jokes.py
```

`GET http://localhost:8000/joke?topic=python`

---

Interactive docs available at `http://localhost:8000/docs`.
