# Agent Eval

## Config File `.agnet-eval.json`

```json
{
  "evalDir": "evalution", // default, support glob
}
```

## Dir Structure

```md
|- evalution                  // root dir
 |-- agent-name               // agent dir contain all eval cases need exec
   | system-prompt.eval.json  // eval agent's system-prompt for the agent
   |-- case-1                 // case 1 by agent
     |-- metadata.json        // optional
     |-- data.json            // original data
     |-- output.expect.json   // expected output
     |-- output.json          // agent output
     |-- eval.json            // compare agent output and exptected output, and give a score
   |-- case-2
     |-- data.json
     |-- output.expect.json
     |-- output.json
     |-- eval.json
  |-- reports                 // eval report generated after all eval processed
    |-- summary.json
```

## Commands

```bash
## Eval specified agent
eval <agent-name>

## Eval specified agent and case
eval <agent-name> -t <case-name>

## Eval All
eval --all

## Only generated agent output
eval <agent-name> --only-output

## Only Eval output
eval <agent-name> --only-eval
```

## Config on package.json

```json
{
  "scripts": {
    "eval": "agent-eval"
  }
}
```
