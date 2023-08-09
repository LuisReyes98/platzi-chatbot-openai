# Platzi Chatbot with OpenAI

Chatbot con finetunning utilizando el modelo de Davinci de OpenAI

```sh
openai api fine_tunes.create -t data_prepared.jsonl -m davinci
```

Add api key to CLI

```sh
export OPENAI_API_KEY=<api_key>
```

Follow Fine tuning

```sh
openai api fine_tunes.follow -i ft-ouK0qOeoDYCGb7MeWCt0FoLU
```

```
[2023-08-05 22:51:19] Created fine-tune: ft-ouK0qOeoDYCGb7MeWCt0FoLU
[2023-08-06 01:17:18] Fine-tune costs $1.80
[2023-08-06 01:17:18] Fine-tune enqueued. Queue number: 0
[2023-08-06 01:17:20] Fine-tune started
[2023-08-06 01:21:38] Completed epoch 1/4
[2023-08-06 01:22:38] Completed epoch 2/4
[2023-08-06 01:23:38] Completed epoch 3/4
[2023-08-06 01:24:38] Completed epoch 4/4
[2023-08-06 01:25:20] Uploaded model: davinci:ft-personal-2023-08-06-05-25-19
[2023-08-06 01:25:21] Uploaded result file: file-6gE21Kgi39Gpperso8FkTVlP
[2023-08-06 01:25:21] Fine-tune succeeded

Job complete! Status: succeeded 🎉
Try out your fine-tuned model:

openai api completions.create -m davinci:ft-personal-2023-08-06-05-25-19 -p <YOUR_PROMPT>
```
