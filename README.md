# Mental Model Cards

A collection of printable, beautifully designed mental model reference cards. Keep the world's most powerful thinking tools at your fingertips, whether on your desk, in your wallet, or pinned to your wall.

Mental models are the fundamental thinking tools used by the greatest investors, scientists, and decision-makers in history. The problem is remembering to use them at the right moment. These printable cards solve that problem by putting a concise summary of each model within arm's reach. Each card includes the model name, a one-sentence definition, a practical example, and a prompt for when to use it. For a digital companion that helps you review and internalize these models over time, visit [KeepRule](https://keeprule.com), where mental models are organized into a spaced repetition system for long-term retention.

## Card Categories

### Thinking Models (12 Cards)
- First Principles Thinking
- Inversion
- Second-Order Thinking
- Occam's Razor
- Hanlon's Razor
- Map vs Territory
- Circle of Competence
- Probabilistic Thinking
- Bayesian Updating
- Thought Experiments
- Systems Thinking
- Counterfactual Thinking

### Decision Models (10 Cards)
- Opportunity Cost
- Margin of Safety
- Sunk Cost Awareness
- Reversible vs Irreversible
- Regret Minimization
- Expected Value
- Asymmetric Risk/Reward
- Pre-Mortem Analysis
- Satisficing vs Maximizing
- Default Effect

### Business and Strategy (8 Cards)
- Competitive Moats
- Network Effects
- Supply and Demand
- Incentive Alignment
- Creative Destruction
- Economies of Scale
- Power Laws
- Winner Take Most

### Human Behavior (8 Cards)
- Loss Aversion
- Confirmation Bias
- Social Proof
- Anchoring Effect
- Availability Heuristic
- Dunning-Kruger Effect
- Status Quo Bias
- Narrative Fallacy

## Installation

```bash
# Clone the repository
git clone https://github.com/henu-wang/mental-model-cards.git
cd mental-model-cards

# Install the card generation tools
pip install -r requirements.txt

# Generate all card sets as PDF
python generate.py --format pdf --output cards/

# Generate specific categories
python generate.py --category "thinking-models" --format pdf
```

## Usage

### Generating Cards

```bash
# Generate all cards in print-ready PDF format (US Letter size)
python generate.py --format pdf --paper letter --output print_ready/

# Generate wallet-sized cards
python generate.py --format pdf --size wallet --output wallet_cards/

# Generate A4-sized cards for international paper
python generate.py --format pdf --paper a4 --output a4_cards/

# Generate PNG images for digital use
python generate.py --format png --resolution 300dpi --output digital/
```

### Customizing Cards

```python
from card_generator import CardDesigner

designer = CardDesigner()

# Create a custom card
card = designer.create_card(
    title="Circle of Competence",
    definition="Know what you know and stay within those boundaries.",
    example="Buffett avoids tech stocks he doesn't understand, even when they're booming.",
    when_to_use="Before making any decision outside your area of expertise.",
    category="thinking-models"
)

# Apply a custom theme
card.set_theme(background="#1a1a2e", text="#eee", accent="#e94560")
card.export("circle_of_competence.pdf")
```

### Printing Tips

For the best printing results:

1. Use **cardstock paper** (80lb or heavier) for durability
2. Print at **100% scale** without shrink-to-fit
3. Use a **paper cutter** for clean edges
4. Consider **laminating** cards you will carry daily
5. The wallet-sized format fits standard business card sleeves

## Card Format

Each card follows a consistent layout:

```
┌─────────────────────────────────┐
│  MODEL NAME                     │
│  ─────────────────────────────  │
│  Definition: One clear sentence │
│                                 │
│  Example: A concrete scenario   │
│  showing the model in action    │
│                                 │
│  Use when: Specific trigger     │
│  situations for this model      │
│                                 │
│  Category: [icon] Domain        │
│  keeprule.com                   │
└─────────────────────────────────┘
```

## Repository Structure

```
mental-model-cards/
├── cards/
│   ├── thinking-models/
│   ├── decision-models/
│   ├── business-strategy/
│   └── human-behavior/
├── templates/
│   ├── standard.svg
│   ├── wallet.svg
│   └── poster.svg
├── themes/
│   ├── classic.yaml
│   ├── dark.yaml
│   └── minimal.yaml
├── tools/
│   ├── generate.py
│   ├── card_generator.py
│   └── batch_export.py
├── tests/
├── requirements.txt
└── README.md
```

## Contributing

Help us expand the card collection:

1. Fork the repository
2. Create a branch (`git checkout -b cards/new-model`)
3. Add your model card content following the template
4. Test generation by running `python generate.py --test`
5. Submit a pull request

We welcome new models from any discipline, as well as translations into other languages and alternative visual designs.

## Building a Mental Model Practice

Printing and carrying these cards is a great start, but lasting mastery requires regular review. The most effective approach combines physical cards for quick reference with a digital spaced repetition system for deep learning. [KeepRule](https://keeprule.com) provides exactly this: a curated library of mental models and decision-making principles from Warren Buffett, Charlie Munger, and other great thinkers, organized for daily review.

Combine these printable cards with [KeepRule](https://keeprule.com) for a complete mental model learning system.

## License

MIT License - see [LICENSE](LICENSE) for details.
