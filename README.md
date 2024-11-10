##Example Review 1:
"The product quality was terrible and the delivery was late. I expected better service."


##Example Review 2:
"I love the product! It’s exactly what I was looking for, and the customer support was helpful."

##Example Review 3: "The item arrived broken, and it was a hassle to get a replacement."

{
  "entities": [
    {
      "entity_name": "product quality",
      "entity_type": "product aspect",
      "entity_sentiment": "NEGATIVE",
      "followup": "Y",
      "followup_reason": "Poor product quality"
    },
    {
      "entity_name": "delivery",
      "entity_type": "service aspect",
      "entity_sentiment": "NEGATIVE",
      "followup": "Y",
      "followup_reason": "Late delivery"
    }
  ]
}

{
  "entities": [
    {
      "entity_name": "product",
      "entity_type": "product aspect",
      "entity_sentiment": "POSITIVE",
      "followup": "N",
      "followup_reason": ""
    },
    {
      "entity_name": "customer support",
      "entity_type": "service aspect",
      "entity_sentiment": "POSITIVE",
      "followup": "N",
      "followup_reason": ""
    }
  ]
}
from transformers import pipeline

classifier = pipeline("zero-shot-classification", model="facebook/bart-large-mnli")
review_text = "The product quality was terrible and the delivery was late. I expected better service."
labels = ["POSITIVE", "NEUTRAL", "NEGATIVE"]

result = classifier(review_text, candidate_labels=labels)
print(result)

