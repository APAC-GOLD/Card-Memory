## WEB3_MEMORY_GAME_DOUBLE_OR_NOTHING_(VSCODE_TESTADMINIA)
Amy Newkirk, Information Lead, 2025 April 29
Time: 2–3 hours total, programming: 1 hour, Unit Tests: 1–2 hours.
Create a working Web3 card game like you're making toast—with just a few more steps and fewer crumbs.
## SECTIONS
DIAGRAM: File Directory Structure
Frontend
Backend
VS Code structure for new feature files
How the Game Works
Improvement Suggestions
Base Environment SETUP Steps
Additional Improvement: Testadminia Memory Game
Double or Nothing Feature Integration
Service design and customer engagement improvement
Credit Context File
What it does: Manages user credit balance
File type: .tsx
Language: React + TypeScript
Extensions required: Prettier, ESLint (recommended)
Code included
All-In Component
What it does: Handles user interaction with the Double or Nothing button
Code included
Extensions and tools used (e.g. Prettier, TypeScript compiler, MongoDB plugin)
Frontend Integration – game.tsx and app.tsx
How the feature connects to existing components
Backend Endpoints
Additions to api.ts if any data routing is required
Sample Express endpoint format
Logic Framework – KPIs & Engagement Tools
How to Track the Impact of This Feature
NPS feedback slider (0–10 scale)
Likert questions for UX clarity and replay intention
Credit usage pattern tracking
Backend log to record the All In interaction frequency
Engagement & User Experience Metrics
(Integrated from NPS and Likert Tools)
Code snippets for NPS/Likert data collection
Extensions and tools used
Test the Code
Extensions and tools used (e.g. Prettier, TypeScript compiler, MongoDB plugin)
Test TypeScript + Jest, for context, for components, for edge use cases, like negative credit
AllInComponent
CardComponent
API GET /cardsx
CreditContext
Test MongoDB
MongoDB insertion
Sources
## FILE DIRECTORY STRUCTURE
root/
├── backend/
│   ├── index.ts
│   ├── routes/
│   │   └── api.ts
│   └── tests/
│       ├── api.test.ts
│       ├── APICards.test.ts
│       ├── MongoInsert.test.ts
│       ├── 04-UNIT_TEST_API GET|cards.docx
│       ├── 06-UNIT_TEST_MongoDB Insertion.docx
│       ├── TestResults_API_GetCards.txt
│       ├── TestResults_MongoDB_Insertion.txt
│       └── README.md
├── frontend/
│   ├── index.html
│   ├── vite.config.ts
│   ├── package.json
│   ├── src/
│   │   ├── App.tsx
│   │   ├── Game.tsx
│   │   ├── main.tsx
│   │   ├── components/
│   │   │   ├── AllIn.tsx
│   │   │   ├── Card.tsx
│   │   │   ├── 02-UNIT_TEST_AllInComponent.docx
│   │   │   ├── 03-UNIT_TEST_CardComponent.docx
│   │   │   ├── TestResults_AllInComponent.txt
│   │   │   ├── TestResults_CardComponent.txt
│   │   │   └── README.md
│   │   ├── context/
│   │   │   ├── CreditContext.tsx
│   │   │   ├── 05-UNIT_TEST_CreditContext.docx
│   │   │   ├── TestResults_CreditContext.txt
│   │   │   └── README.md
│   │   ├── MemoryCardGame/
│   │   │   ├── MemoryCardGame.tsx
│   │   │   ├── CardUtils.tsx
│   │   │   ├── Play.tsx
│   │   │   └── MemoryEasy.tsx
│   │   └── tests/
│   │       ├── AllInComponent.test.tsx
│   │       ├── CardComponent.test.tsx
│   │       ├── CreditContext.test.tsx
│   │       └── README.md
│   └── assets/
│       └── images/
│           └── audio/
├── README.md
├── package.json
├── 01-WEB3_MEMORY_GAME_DOUBLE_OR_NOTHING_(VSCODE_TESTADMINIA).docx
└── AmyNewkirkTechLead.png
## HOW THE GAME WORKS
## (OR HOW IT’S SUPPOSED TO IF CODE BEHAVES)
The TESTADMINIA Card Memory Game is a digital twist on the classic memory match game. Here’s the jazz breakdown:

You open the app at http://localhost:5173. It greets you with a grid of cards—face down, pretending to be mysterious

Click one card. It flips and reveals its identity—maybe it’s a banana, perhaps a blockchain symbol

Click a second card. It flips, too. If it’s a match with the first, you win the round. If not, both flip back like they’re embarrassed

The goal? Match all the pairs with the fewest moves (and the least muttered profanity)

Each match may reward you with a token if Web3 and MetaMask integration are active. That’s the incentive part—play to earn, or at least play to justify staring at your screen

Under the hood, React handles the frontend state (like card flips and score tracking), Node.js/Express handles the backend (like storing game sessions or player data), and MongoDB can persist leaderboard info or matched card history if you want to get fancy

The MetaMask/Web3 integration lets you sign in with your wallet and maybe earn ERC-20 or in-game tokens, depending on how far you take the incentive model

## IMPROVEMENTS SUGGESTIONS
Image showing - Executive Summary of Improvements


The game has more layers than a lasagna: Flatten the architecture by consolidating logic in the frontend or the backend.

Avoid brain freeze: use TypeScript for fewer bugs and better maintainability.

It’s a guessing contest, but let’s not guess user traffic: Monitor and optimize performance before complaints pile up

Web3 incentives should be more than smoke and mirrors: clarify tokenomics and illustrate the potential gains.

Add monitoring and tracing using AWS CloudWatch or X-Ray: You’ll want breadcrumbs when users start yelling.

Don’t ignore latency: Implement retries with exponential backoff for Web3 wallet interactions.

Use availability zones for your backend if you ever host this on AWS: Think earthquake insurance for servers.

Incorporate test coverage reports with nyc or jest—coverage: It’s like flossing for code.

Refactor API calls to be event-driven if possible. AWS recommends a decoupled design using pub/sub (like SNS, SQS): Think walkie-talkie, not conference call

Replace hardcoded strings and values: Use environment variables like .env and dotenv.

Avoid spaghetti imports by using absolute paths: vite.config.ts can help

Create a fallback route in the frontend to catch 404s: Users will click everything—even the corners.

Store tokenomics models (if they exist) in JSON, versioned in the repo, so they evolve with your game economy.

## ADDITIONAL IMPROVEMENT: INCREASE THE STAKES
—> Service Design and Customer Engagement Improvement.
ALL-IN - Double or Nothing Integration
## BASE ENVIRONMENT STEPS
Install Visual Studio Code from code.visualstudio.com

Install Node.js from nodejs.org, then restart your computer like it’s 2004

Open Terminal (Mac) or PowerShell (Windows). Paste this in:
git clone https://github.com/testadminia/Card-Memory.git

Change into the project folder
cd Card-Memory

Open VS Code with the project
code.

In the VS Code sidebar, open the frontend folder. Look for App.jsx or App.tsx. If it’s JavaScript, rename files and convert to TypeScript (.tsx). Update syntax using type annotations to reduce developer panic attacks

Install dependencies for the frontend and backend. Run this from Terminal inside the frontend:
npm install

And now for backend:
cd ../backend
npm install

Start the backend server:
npm start

Now back to frontend:
cd ../frontend
npm start

Open http://localhost:5173 in your browser. If it explodes, check the Terminal logs—it’s not judging you, just guiding

Replace all JavaScript files in the frontend with TypeScript. Add types, interfaces, and maybe a motivational quote

Flatten your folder structure if you see things like /frontend/src/components/ui/cards/flip/hover/Layer7.js. Move files where they make sense, not where they multiply

Set up unit testing with Vitest or Jest. In frontend:
npm install –save-dev vitest @testing-library/react

Create Card.test.tsx under frontend/src/__tests__/. Add a test like:
‘’
```ts
import { describe, it, expect } from 'vitest'
import Card from '../components/Card'

describe('Card', () => {
it('renders without crashing', () => {
```
expect(Card).toBeTruthy()
})
})

‘’

Run tests:
npx vitest

API testing? Use Postman or just a browser for GETs. Create integration tests in the backend using:
npm install –save-dev jest supertest

Create a test file, api.test.js and write a sample:
‘’
```ts
const request = require('supertest')
const app = require('../index')

describe('GET /cards', () => {
it('returns card data', async () => {
const response = await request(app).get('/cards')
```
expect(response.statusCode).toBe(200)
})
})

To test MongoDB, first check your connection string. Try connecting with mongosh or using MongoDB Compass. Insert dummy data using:

```ts
use cardGame
db.cards.insertOne({ name: 'Spade', value: 'A' })

```
Confirm it’s in there:

```ts
db.cards.find()

```
‘’

## TIP:
Don’t forget to document all your changes. The GitHub README is your therapy session. Keep it honest and clear.


## TESTADMINIA MEMORY GAME – DOUBLE OR NOTHING FEATURE INTEGRATION
This guide walks you through modifying the TESTADMINIA Card Memory Game to add a 'Double or Nothing' feature, built with TypeScript and React in VS Code.
It includes setup steps, context integration, and UI elements for gameplay credits.

## SETUP AND MODIFICATION STEPS
## EXTENSIONS AND TOOLS USED
VS Code: VS Code, .tsx file type, React, Node.js, MongoDB, Vite, TypeScript, Prettier turned on.

Credit Context File
What it does: Manages user credit balance
File type: .tsx
Language: React + TypeScript
Extensions required: Prettier, ESLint (recommended)
Code included

All-In Component
What it does: Handles user interaction with the Double or Nothing button
Code included
Extensions and tools used (e.g. Prettier, TypeScript compiler, MongoDB plugin)

Install VS Code and Node.js. Open a terminal or PowerShell and run the following:
git clone https://github.com/testadminia/Card-Memory.git
cd Card-Memory
code.

Install dependencies for both frontend and backend:
cd frontend
npm install
cd ../backend
npm install

Start servers:
npm start (in backend)
npm start (in frontend)


STEP 1 | ADD A CREDIT CONTEXT (CreditContext.tsx)
Create the context to track and modify player credits
Create a new file in frontend/src/context/CreditContext.tsx
VS Code, .tsx file type, React, TypeScript
''
```ts
import React, { createContext, useContext, useState } from 'react'

```
type CreditContextType = {
credits: number
```ts
setCredits: (val: number) => void
```
}

```ts
const CreditContext = createContext<CreditContextType | undefined>(undefined)

export const CreditProvider: React.FC<{ children: React.ReactNode }> = ({ children }) => {
const [credits, setCredits] = useState(100) // Starting balance

```
return (
<CreditContext.Provider value={{ credits, setCredits }}>
{children}
</CreditContext.Provider>
)
}

```ts
export const useCredit = () => {
const context = useContext(CreditContext)
```
if (!context) {
throw new Error('useCredit must be used within a CreditProvider')
}
return context
}

Wrap the app in main.tsx

```ts
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App'
import { CreditProvider } from './context/CreditContext'

```
ReactDOM.createRoot(document.getElementById('root')!).render(
<React.StrictMode>
<CreditProvider>
<App />
</CreditProvider>
</React.StrictMode>
)
''


This component adds the button and logic to double or reset credits:

```ts
''
import React, { useState } from 'react'
import { useCredit } from '../context/CreditContext'

const AllIn: React.FC<{ onResult: (won: boolean) => void }> = ({ onResult }) => {
  const { credits, setCredits } = useCredit()
  const [message, setMessage] = useState('')

  const goAllIn = () => {
    if (credits <= 0) {
      setMessage("You’ve got nothing to bet but your hopes.")
      return
    }

    const win = Math.random() < 0.5
    if (win) {
      setCredits(credits * 2)
      setMessage('Lucky flip! You doubled your credits.')
    } else {
      setCredits(0)
      setMessage('Ouch. Lost it all. Time to earn it back.')
    }
    onResult(win)
  }

  return (
    <div>
      <button onClick={goAllIn}>Go ALL IN (Double or Nothing)</button>
      <p>{message}</p>
    </div>
  )
}

export default AllIn
‘’

```
STEP 2 | CREATE THE “ALL IN” COMPONENT (AllIn.tsx)
This component adds the button and logic to double or reset credits.
In frontend/src/components/AllIn.tsx
VS Code, .tsx file type, React, TypeScript
''
```ts
import React, { useState } from 'react'
import { useCredit } from '../context/CreditContext'

const AllIn: React.FC<{ onResult: (won: boolean) => void }> = ({ onResult }) => {
const { credits, setCredits } = useCredit()
const [message, setMessage] = useState('')

const goAllIn = () => {
```
if (credits <= 0) {
setMessage("You’ve got nothing to bet but your hopes.")
return
}

```ts
const win = Math.random() < 0.5 // 50/50 chance
```
if (win) {
setCredits(credits * 2)
setMessage('Lucky flip! You doubled your credits.')
} else {
setCredits(0)
setMessage('Ouch. Lost it all. Time to earn it back.')
}
onResult(win)
}

return (
<div>
<button onClick={goAllIn}>Go ALL IN (Double or Nothing)</button>
<p>{message}</p>
</div>
)
}

export default AllIn
''

STEP 3 | INTEGRATE INTO GAME UI (Game.tsx)
In Game.tsx or wherever your main game board logic lives.
VS Code, .tsx file type, React, TypeScript
```ts
'' 
import AllIn from './components/AllIn'
import { useCredit } from './context/CreditContext'

const Game: React.FC = () => {
  const { credits } = useCredit()

  const handleAllInResult = (won: boolean) => {
    console.log(won ? 'Double it up!' : 'Back to square one.')
  }

  return (
    <div>
      <h2>Credits: {credits}</h2>
      <AllIn onResult={handleAllInResult} />
      {/* Rest of your game board here */}
    </div>
```
''


## NOW YOU’VE GOT A FUNCTIONING “ALL IN” MECHANIC

Users can press the “All In” button like they’re in a smoky Vegas room, risking everything for a double or a wipeout. It’s a fun way to gamify courage… or punish recklessness.
## LOGIC FRAMEWORK – IMPACT & MEASUREMENT
Use to check the user engagement and impact of the “Double or Nothing” Feature.
CLEAR GOAL FOR CHANGE:
Increase player engagement through higher-risk gameplay options

DESCRIPTION OF THE PROBLEM:
Players lose interest after memorizing card mechanics without further incentives

KEY STRATEGIES TO DRIVE CHANGE:
Implement 50/50 Double or Nothing mechanic to gamify credit management
Track decision outcomes and player behavior using backend logs

GUIDING PRINCIPLES FOR GROUP BEHAVIOR:
Transparency of odds and credit consequences
Encourage experimentation without real currency risk

EVALUATION APPROACH:
Net Promoter Score and Likert responses in-game
Track credit reset/reward patterns and average retention time
Record frequency of All In use per session to assess risk behavior
## TEST THE CODE
These tests validate the credit context and AllIn component logic. Uses Jest and React Testing Library.

Test TypeScript + Jest, for context, for components, for edge use cases, like negative credit.
AllInComponent
CardComponent
API GET /cardsx
CreditContext

Test MongoDB
MongoDB Insertion



## ALL IN COMPONENT UNIT TEST
TEST FILE TYPE: .test.tsx
FRAMEWORKS REQUIRED: Jest, React Testing Library
Validates user interaction logic with the Double or Nothing button.
''
```ts
import { render, fireEvent } from '@testing-library/react'
import AllIn from '../components/AllIn'
import { CreditProvider } from '../context/CreditContext'

test('renders without crashing', () => {
  render(
    <CreditProvider>
      <AllIn onResult={() => {}} />
    </CreditProvider>
  )
})

test('goAllIn updates credits or resets', () => {
  const onResultMock = jest.fn()
  const { getByText } = render(
    <CreditProvider>
      <AllIn onResult={onResultMock} />
    </CreditProvider>
  )
  const button = getByText(/double or nothing/i)
  fireEvent.click(button)
  expect(onResultMock).toHaveBeenCalled()
})

```
''

## CARD COMPONENT UNIT TEST
TEST FILE TYPE: .test.tsx
FRAMEWORKS REQUIRED: Jest, React Testing Library
Validates that a card renders correctly and hides content when not flipped.
''
```ts
import { render, screen } from '@testing-library/react'
import CardComponent from '../components/CardComponent'

test('renders a card with correct props', () => {
```
render(<CardComponent id="card1" content="Memory A" flipped={false} />)
expect(screen.getByText(/Memory A/i)).toBeInTheDocument()
})

```ts
test('does not show content when card is not flipped', () => {
```
render(<CardComponent id="card2" content="Secret" flipped={false} />)
expect(screen.queryByText('Secret')).toBeNull()
})

''

API ENDPOINT TEST – GET /cardsx
TEST FILE TYPE: .test.ts
FRAMEWORKS REQUIRED: Jest, Supertest, Express
Validates that the /cardsx endpoint returns a list of cards with the expected structure.
''
```ts
import request from 'supertest'
import app from '../api' // Make sure Express app is exported

describe('GET /cardsx', () => {
it('should return 200 and an array of cards', async () => {
const res = await request(app).get('/cardsx')
```
expect(res.statusCode).toBe(200)
expect(Array.isArray(res.body)).toBe(true)
expect(res.body[0]).toHaveProperty('id')
expect(res.body[0]).toHaveProperty('content')
})
})

''

## CREDIT CONTEXT UNIT TEST
This file tracks and modifies the user's credit value using React Context; It requires TypeScript and React extensions.
Validates the CreditContext provider and hook logic.
TEST FILE TYPE:  .test | .ts
FRAMEWORKS REQUIRED:  Jest, React Testing Library

''
```ts
import { renderHook, act } from '@testing-library/react-hooks'
import { CreditProvider, useCredit } from '../context/CreditContext'

test('initial credits are 100', () => {
  const wrapper = ({ children }) => <CreditProvider>{children}</CreditProvider>
  const { result } = renderHook(() => useCredit(), { wrapper })
  expect(result.current.credits).toBe(100)
})

test('can update credits', () => {
  const wrapper = ({ children }) => <CreditProvider>{children}</CreditProvider>
  const { result } = renderHook(() => useCredit(), { wrapper })
  act(() => {
    result.current.setCredits(200)
  })
  expect(result.current.credits).toBe(200)
})

```
''

Validates the CreditContext provider and hook logic:
''
```ts
import React, { createContext, useContext, useState } from 'react'

type CreditContextType = {
  credits: number
  setCredits: (val: number) => void
}

const CreditContext = createContext<CreditContextType | undefined>(undefined)

export const CreditProvider: React.FC<{ children: React.ReactNode }> = ({ children }) => {
  const [credits, setCredits] = useState(100)
  return (
    <CreditContext.Provider value={{ credits, setCredits }}>
      {children}
    </CreditContext.Provider>
  )
}

export const useCredit = () => {
  const context = useContext(CreditContext)
  if (!context) throw new Error('useCredit must be used within a CreditProvider')
  return context
}


```
''

## MONGODB INSERTION TEST
TEST FILE TYPE: .test.ts
FRAMEWORKS REQUIRED: Jest, MongoDB
Validates insertion of user credit data into MongoDB and ensures the document is saved correctly.
''
```ts
import { MongoClient } from 'mongodb'

const uri = 'mongodb://localhost:27017'
const dbName = 'testadminia'
const collection = 'credits'

describe('MongoDB credit insertion', () => {
```
let client

```ts
beforeAll(async () => {
```
client = new MongoClient(uri)
await client.connect()
})

```ts
afterAll(async () => {
```
await client.db(dbName).collection(collection).deleteMany({})
await client.close()
})

```ts
test('inserts a credit record successfully', async () => {
const db = client.db(dbName)
const result = await db.collection(collection).insertOne({ userId: 'abc123', credit: 150 })
```
expect(result.insertedId).toBeDefined()
})
})

''

## SOURCES
https://aws.amazon.com/builders-library/static-stability-using-availability-zones/
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.Scenarios.html
https://github.com/awsdocs/aws-doc-sdk-examples/blob/d73001daea05266eaa9e074ccb71b9383832369a/python/README.md
https://github.com/testadminia/Card-Memory.git Branch: APAC-GOLD
https://icograms.com/usage-software-architecture-diagram#:~:text=Icograms%20Designer%20offers%20a%20user,of%20creating%20software%20architecture%20diagrams
https://kubernetes.io/docs/reference/kubectl/quick-reference/
https://medium.com/edureka/aws-architect-interview-questions-5bb705c6b660
https://serverlessland.com/event-driven-architecture/visuals/common-issued-with-eda
https://www.dataquest.io/blog/unit-tests-python/