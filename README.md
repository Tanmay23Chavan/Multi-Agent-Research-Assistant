# Multi-Agent Research Assistant

A sophisticated multi-agent system for automated research, analysis, and report generation using LLMs and tool integration.

## Features

- **Multiple Specialized Agents**: Research, Analysis, Summarization, and Report Generation agents
- **Autonomous Task Planning**: Agents automatically plan and execute tasks
- **Web Search Integration**: Real-time information retrieval capabilities
- **Document Processing**: Support for multiple document formats
- **Intelligent Caching**: Results caching to optimize API usage
- **Comprehensive Logging**: Full audit trail of agent activities
- **REST API**: Easy integration with external systems
- **Docker Support**: Containerized deployment

## Architecture

```
Multi-Agent Research Assistant
├── Core Agents
│   ├── Research Agent
│   ├── Analysis Agent
│   ├── Summarization Agent
│   └── Report Generation Agent
├── Tool Systems
│   ├── Web Search Tools
│   ├── Document Processing
│   ├── Database Management
│   └── Cache Management
├── Orchestration
│   ├── Task Planner
│   ├── Agent Coordinator
│   └── Workflow Manager
└── APIs & Interfaces
    ├── REST API
    ├── CLI Interface
    └── Web Dashboard
```

## Quick Start

### Prerequisites
- Python 3.9+
- OpenAI API Key
- Redis (optional, for caching)

### Installation

```bash
git clone https://github.com/Tanmay23Chavan/Multi-Agent-Research-Assistant.git
cd Multi-Agent-Research-Assistant
pip install -r requirements.txt
```

### Configuration

Create `.env` file:

```env
OPENAI_API_KEY=your_api_key_here
RESEARCH_MODEL=gpt-4
ANALYSIS_MODEL=gpt-4
SUMMARIZATION_MODEL=gpt-3.5-turbo
REPORT_MODEL=gpt-4
REDIS_URL=redis://localhost:6379/0
LOG_LEVEL=INFO
```

### Usage

```python
from multi_agent_research import ResearchAssistant

# Initialize assistant
assistant = ResearchAssistant()

# Execute research task
result = assistant.research("Machine Learning trends in 2024")

# Get results
print(result.summary)
print(result.analysis)
print(result.report)
```

### API Endpoints

- `POST /api/research` - Start research task
- `GET /api/tasks/{task_id}` - Get task status
- `GET /api/results/{task_id}` - Get results
- `POST /api/analyze` - Analyze content
- `POST /api/summarize` - Summarize content
- `POST /api/generate-report` - Generate report

## Project Structure

```
src/
├── agents/
│   ├── base_agent.py
│   ├── research_agent.py
│   ├── analysis_agent.py
│   ├── summarization_agent.py
│   └── report_agent.py
├── tools/
│   ├── web_search.py
│   ├── document_processor.py
│   ├── cache_manager.py
│   └── database.py
├── orchestration/
│   ├── task_planner.py
│   ├── agent_coordinator.py
│   └── workflow_manager.py
├── api/
│   ├── server.py
│   ├── routes.py
│   └── schemas.py
├── utils/
│   ├── logger.py
│   ├── config.py
│   └── helpers.py
└── main.py
```

## Development

### Running Tests

```bash
pytest tests/ -v
```

### Running Locally

```bash
python src/main.py
```

### Docker

```bash
docker build -t multi-agent-research .
docker run -p 8000:8000 --env-file .env multi-agent-research
```

## Documentation

- [Agent Design](docs/agents.md)
- [Tool Integration](docs/tools.md)
- [API Reference](docs/api.md)
- [Configuration](docs/config.md)

## Contributing

1. Create feature branch (`git checkout -b feature/amazing-feature`)
2. Commit changes (`git commit -m 'Add amazing feature'`)
3. Push to branch (`git push origin feature/amazing-feature`)
4. Open Pull Request

## License

MIT License - see LICENSE file for details

## Author

Tanmay Chavan
