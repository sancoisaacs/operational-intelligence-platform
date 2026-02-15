# AdherenceFlow v4 | Analyst Edition

**AI-Powered Workforce Adherence Analysis**  
*Local LLM Integration • Zero Cloud Costs • Complete Privacy*

---

## 🎯 What It Does

AdherenceFlow helps operations managers identify, analyze, and address employee adherence issues **before they become disciplinary problems**.

### The Problem It Solves

Most managers treat adherence violations as discipline issues. They coach, they warn, they escalate. But they rarely ask: **"What's the root cause?"**

AdherenceFlow combines:
- ✅ **Pattern Detection** - Identifies chronic vs. first-time offenders
- ✅ **AI Analysis** - Connects to local Ollama for intelligent insights
- ✅ **Root Cause Exploration** - Helps managers ask the right questions
- ✅ **Coaching Tools** - Generates context-aware conversation starters (not scripts)

---

## 🚀 Quick Start

### Requirements
- Any computer with a web browser
- **Ollama** installed and running (for AI features)

### Setup (3 Steps)

**1. Install Ollama**
```bash
# Linux/Mac
curl https://ollama.ai/install.sh | sh

# Or download from: https://ollama.com
```

**2. Start Ollama & Pull a Model**
```bash
ollama serve

# In another terminal
ollama pull mistral:7b
# Or for faster responses on mobile: ollama pull qwen:0.5b
```

**3. Open AdherenceFlow**
- Download `AdherenceFlow_v4.html`
- Open in Chrome/Firefox
- Click "Connect to Ollama"
- Done ✅

**No web server needed. Just open the HTML file.**

---

## 📊 Features

### Core Analytics
- **Violation Detection** - Auto-flags break/lunch overages
- **Historical Tracking** - Shows patterns over time (first offense vs. chronic)
- **Sparkline Visualizations** - Quick visual history per agent
- **Risk Classification** - Clean → Pattern → Chronic
- **Adherence Scoring** - Team-wide metrics

### AI Assistant (Ollama Integration)
- **Natural Language Queries** - Ask questions about your data
- **Pattern Analysis** - AI identifies trends you might miss
- **Root Cause Suggestions** - Goes beyond "they're late"
- **Report Generation** - Creates summary reports on demand

### Manager Tools
- **Coaching Queue** - Prioritizes who needs attention
- **Context Cards** - Shows full history when coaching
- **Note Templates** - Tone-adjusted based on severity
- **Export Options** - Copy tables for reporting

---

## 🎓 How To Use

### 1. Load Your Data

**Option A: Upload CSV**
```csv
Agent,Period,Week,Break Time,Break2 Time,Break3 Time,Lunch Time,Personal Time
John Doe,2024-02-15,7,00:18:00,00:15:00,00:15:00,00:58:00,00:05:00
```

**Option B: Use Sample Data**
- Click "Load Sample Team" to test with demo data

### 2. Review Dashboard
- **Week Number** - Current period
- **Adherence Score** - % of compliant time entries
- **Repeat Offenders** - Count of chronic issues
- **Total Records** - Historical data size

### 3. Check Coaching Queue
Red cards = Need immediate attention  
Yellow cards = Emerging patterns  
Green cards = First-time issues  

### 4. Ask The AI
**Good Questions:**
- "Who needs coaching this week?"
- "What patterns do you see in Sarah's breaks?"
- "Why might someone consistently go over on Break 1?"
- "Summarize the chronic issues"

**Better Questions (Root Cause Focused):**
- "What environmental factors might cause Break 1 overages?"
- "If someone is consistently late from lunch, what could be happening?"
- "How would you approach coaching a pattern vs. a chronic issue?"

### 5. Generate Context-Aware Notes
- Click "Note" on any violation
- System suggests tone (Supportive/Direct/Formal)
- Edit to match your voice
- Copy to clipboard

---

## 🧠 Using The AI Effectively

### The AI Model Matters

**For Speed (Mobile/Low-Spec PC):**
```bash
ollama pull qwen:0.5b      # Fast, basic reasoning
```

**For Quality (Desktop/Server):**
```bash
ollama pull mistral:7b     # Best balance
ollama pull llama3:70b     # Maximum insight (needs powerful GPU)
```

### Sample Prompts

**Diagnostic:**
- "List all agents with 3+ violations"
- "What's the most common violation type?"
- "Compare this week to last week"

**Root Cause:**
- "Why might multiple people go over on Break 1?"
- "What external factors could cause lunch overages?"
- "If someone is consistently 3 minutes over, what might be happening?"

**Coaching:**
- "How should I approach a first-time offender?"
- "Write a coaching note for Sarah Jenkins focusing on support, not discipline"
- "What questions should I ask someone with chronic Break 2 issues?"

---

## 🏢 Deployment Scenarios

### Solo Analyst (You Right Now)
```
Your Phone:
├─ Termux: ollama serve
└─ Chrome: AdherenceFlow.html
```
**Cost:** $0  
**Privacy:** Complete  

### Small Team (5-10 People)
```
Old Gaming PC (RTX 2070):
├─ Ubuntu + Ollama
├─ Mistral 7B
└─ Accessible at: 192.168.1.50:11434

Employees:
├─ Download HTML file from \\shared\
└─ Open → Auto-connects to internal AI
```
**Hardware Cost:** $0-500 (repurpose old PC)  
**Monthly Cost:** $0  
**vs. Cloud AI:** Saves $300-500/month  

### Enterprise (100+ People)
```
Dedicated Server:
├─ RTX 4090 or A100
├─ Llama 3 70B
└─ Accessible via: http://ai.company.internal:11434

Distribution:
├─ Intranet portal
├─ Or: Email HTML file to all managers
└─ Zero installation required
```
**Hardware Cost:** $3k-10k one-time  
**Savings:** $10k-50k/year vs. cloud AI  

---

## 🔒 Privacy & Compliance

### Data Never Leaves Your Device/Network

**Cloud AI (OpenAI/Anthropic):**
- ❌ Data sent to external servers
- ❌ Subject to their retention policies
- ❌ Requires legal agreements
- ❌ Monthly costs ($$$)

**AdherenceFlow + Ollama:**
- ✅ Processes locally
- ✅ You control the data
- ✅ POPIA/GDPR compliant by design
- ✅ Zero ongoing costs

### For Regulated Industries
- Healthcare: HIPAA-friendly (data stays on-premises)
- Legal: Attorney-client privilege maintained
- Finance: SOX-compliant (audit trail in your control)
- HR: Employee data never exposed to third parties

---

## 🛠️ Technical Details

### Architecture
```
Browser (file://)
    ↓
Fetch API
    ↓
http://localhost:11434/api/generate
    ↓
Ollama (local LLM)
    ↓
Response (JSON)
```

**No web server required.** The HTML file makes direct API calls to Ollama.

### Stack
- **Frontend:** Vanilla HTML/CSS/JS (zero dependencies)
- **Storage:** localStorage (persistent across sessions)
- **AI:** Ollama API (local inference)
- **Compatibility:** Any modern browser

### File Size
- Single HTML file: ~40KB
- No build step
- No npm install
- **Just open and use**

---

## 🎨 Customization

### Change Ollama Server URL

In the header, modify:
```html
<input class="server-input" id="ollamaServer" 
       value="http://localhost:11434">
```

**For company server:**
```
http://192.168.1.50:11434
http://ai.company.internal:11434
```

### Modify Adherence Limits

Find this in the JavaScript:
```javascript
const LIMITS = {
    break: 15 * 60,     // 15 minutes
    lunch: 60 * 60,     // 60 minutes
    personal: 10 * 60   // 10 minutes
};
```

Adjust to match your company policy.

### Styling

Colors are defined in CSS variables at the top:
```css
:root {
    --primary: #2563eb;      /* Blue */
    --red-text: #991b1b;     /* Violation red */
    --green-text: #065f46;   /* Compliant green */
    /* etc. */
}
```

---

## 📖 Use Case: Root Cause Analysis

### Traditional Approach (Discipline-Focused)
```
Manager: "Sarah was late from break 3 times this week."
Action: "Verbal warning."
Result: Behavior may or may not improve.
```

### AdherenceFlow Approach (Root Cause-Focused)
```
Manager: Opens AdherenceFlow
AI Insight: "Sarah's Break 1 overages are consistently 
             2-3 minutes and only on Tuesday/Thursday."
Manager: [Checks pattern] "Hmm, those are clinic days."
Manager to Sarah: "I noticed you're running over on breaks 
                   on clinic days. Is the medical facility 
                   backed up? Do we need to adjust your 
                   schedule?"
Sarah: "Yes! The line is always long on Tuesdays."
Action: Schedule adjustment (not discipline)
Result: Issue resolved permanently.
```

**This is the difference.**

---

## 🚨 Troubleshooting

### "Cannot connect to Ollama"
1. Check Ollama is running: `ollama serve`
2. Verify port 11434 is open
3. Try: `curl http://localhost:11434` (should return JSON)
4. Check firewall settings

### "AI responses are slow"
- Try smaller model: `ollama pull qwen:0.5b`
- Or quantized version: `ollama pull mistral:7b-q4`
- Check GPU/CPU usage during inference

### "AI gives generic answers"
- Provide more context in prompts
- Ask specific questions
- Use "Why?" and "How?" questions
- Try different models (Mistral is best for reasoning)

### "Violations not detected"
- Check CSV column headers match expected format
- Verify time format is HH:MM:SS
- Ensure no extra spaces in data

---

## 📝 Roadmap / Ideas For Improvement

### Manager Enablement
- [ ] **Root Cause Library** - Common patterns and suggested questions
- [ ] **Coaching Scripts** - Not templates, but conversation frameworks
- [ ] **Trend Alerts** - Notify when team-wide patterns emerge
- [ ] **Comparison Tools** - "Is this normal for my team/department?"

### AI Enhancements
- [ ] **Multi-Agent System** - Separate agents for pattern detection, root cause, and coaching
- [ ] **Sentiment Analysis** - Detect stress/burnout signals in patterns
- [ ] **Predictive Alerts** - "Agent X is showing early signs of chronic issues"
- [ ] **Auto-Summarization** - Weekly manager briefing reports

### Integration
- [ ] **Workforce Management Systems** - Import data directly
- [ ] **Calendar Integration** - Consider PTO, training, meetings
- [ ] **Slack/Teams Notifications** - Alert managers to emerging patterns

---

## 💡 Pro Tips

### For Analysts
1. **Historical Context Is Key** - Load several weeks of data to see real patterns
2. **Use AI for "Why"** - Let the data show "what", ask AI for "why"
3. **Export Often** - Copy tables for management reports
4. **Ask Comparative Questions** - "How does this week compare to last week?"

### For Managers
1. **Start Supportive** - First offense = assume good intent
2. **Look for Environmental Factors** - Break room location, lunch queue, system issues
3. **Ask Questions** - "What's happening that's causing this?"
4. **Document Conversations** - Use Note tool to record coaching sessions
5. **Adjust Policies** - If everyone goes over, the policy might be wrong

### For Implementers
1. **Start Small** - Test with 1 department
2. **Train Managers** - Show them how to ask root cause questions
3. **Monitor Adoption** - Who's using it? Who needs help?
4. **Iterate** - Get feedback, improve prompts
5. **Share Wins** - When root cause analysis solves an issue, tell people

---

## 📄 License

MIT License - Use freely, modify as needed, no attribution required.

---

## 🤝 Contributing

Found a bug? Have an idea?  
This is a single HTML file — just edit and share your improvements.

**Particularly interested in:**
- Better AI prompts for root cause analysis
- Manager coaching frameworks
- Integration examples with workforce systems
- Anonymized case studies of successful implementations

---

## 📬 Support

This is an open-source tool with no official support channel.

**For technical issues:**
- Ollama docs: https://ollama.ai
- Check Troubleshooting section above

**For use case questions:**
- Review the "Root Cause Analysis" section
- Try different AI prompts
- Experiment with your own data

---

## 🎯 The Philosophy

**Adherence violations are symptoms, not problems.**

The problem is usually:
- Poor process design
- Unrealistic policies
- Environmental constraints
- Lack of resources
- Communication gaps

**AdherenceFlow helps you find the REAL problem.**

Then you can fix it.

Instead of just disciplining the symptom.

---

*Built by someone who got tired of AI regression bugs and decided to ship anyway.* 😅

**Version:** 4.0  
**Last Updated:** February 2026  
**No cloud. No costs. No hababa.**
