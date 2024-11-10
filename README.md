{ "entities": [
{
      "entity_name": "<entity name>",
      "entity_type": "<entity type>",
      "entity_sentiment": "<entity sentiment>",
      "followup": "<Y or N for follow-up>",
      "followup_reason": "<reason for follow-up>"
    }
  ]
}


Review: "The service was terrible, and the staff was unhelpful. I don't think I'll shop here again."

{
  "entities": [
    {
      "entity_name": "service",
      "entity_type": "aspect",
      "entity_sentiment": "NEGATIVE",
      "followup": "Y",
      "followup_reason": "Customer expressed dissatisfaction with the service quality."
    },
    {
      "entity_name": "staff",
      "entity_type": "aspect",
      "entity_sentiment": "NEGATIVE",
      "followup": "Y",
      "followup_reason": "Customer reported unhelpful staff behavior."
    }
  ]
} 


