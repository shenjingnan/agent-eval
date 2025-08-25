# Agent Eval

## Config File `.agnet-eval.json`

```json
{
  "evalDir": "evalution", // default, support glob
}
```

## Dir Structure
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
