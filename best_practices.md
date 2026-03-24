# Best Practices for Token-Efficient Prompts

## 1. Be Specific and Concise

### ❌ Inefficient
```
Tell me everything about this topic that you know about
```

### ✅ Efficient
```
List 3 key facts about X
```

**Savings: 50% fewer tokens**

---

## 2. Use Structured Output Formats

Instead of narrative explanations, use structured formats:

### JSON Format
```json
{
  "request": "Your specific request",
  "output_format": "json",
  "fields": ["field1", "field2", "field3"]
}
```

### YAML Format
```yaml
request: Your specific request
output_format: yaml
fields:
  - field1
  - field2
```

**Savings: 20-30% fewer tokens in response**

---

## 3. Remove Politeness and Filler

### ❌ Bad
```
Could you please very kindly help me with the following request?
```

### ✅ Good
```
Help with: [request]
```

**Savings: 5-10 tokens per prompt**

---

## 4. Use Templates Over Repetition

### ❌ Bad
```
Translate 'hello' from English to Spanish
Translate 'goodbye' from English to Spanish
```

### ✅ Good
```
Template: "Translate '{text}' from {lang1} to {lang2}"
```

**Savings: 30-40% tokens**

---

## 5. Compress Multimodal Input

### Image Descriptions
```
❌ Long: "A photograph depicting a sunset scene with golden light..."
✅ Short: "Sunset with water reflection"
```

### Audio Transcriptions
```
❌ Full transcript: (2000+ tokens)
✅ Key points: Topic, decisions, action items
```

**Savings: 40-70% tokens**

---

## 6. Batch Similar Requests

**Savings: 50% tokens**

---

## 7. Use Examples Over Explanations

**Savings: 60% tokens**

---

## 8. Be Explicit About Output Format

**Savings: 40% tokens**

---

## Summary

**Golden Rules:**
1. ✂️ Cut ruthlessly
2. 📊 Use structure
3. 🎯 Be specific
4. 📝 Show examples
5. 🔄 Template & batch

**Expected Results:**
- 30-50% token reduction (most cases)
- 60-80% reduction (advanced optimization)
- 10-20% improvement in response time