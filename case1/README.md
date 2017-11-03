# Case 1

## ATC (Acceptance Test Criteria)

- Create ABI with duplicate table names
- Verify ABI will not load

## Command Run
```
eosc create account inita case1 EOS4toFS3YXEQCkuuw1aqDLrtHim86Gz9u3hBdcBw5KNPZcursVHq EOS7d9A3uLe6As66jzN8j44TXJUqJSK3bFjjEEqR4oTvNAB3iM9SA -s
eoscpp -o case1.wast case1.cpp
eosc set contract case1 case1.wast case1.abi -s
```


## Result
```
Reading WAST...
Assembling WASM...
Publishing contract...
2228753ms thread-0   main.cpp:1101                 main                 ] Failed with error: 10 assert_exception: Assert Exception
status_code == 200: Error code 500
: {"code":500,"message":"Internal Service Error","details":"10 assert_exception: Assert Exception\ntables.size() == abi.tables.size(): \n    {}\n    thread-0  AbiSerializer.cpp:129 setAbi\n\n    {\"context.msg\":{\"code\":\"eos\",\"type\":\"setcode\",\"authorization\":[{\"account\":\"case1\",\"permission\":\"active\"}],\"data\":\"0000000080a0b0410000f1010061736d0100000001110460017f0060017e0060000060027e7e00021b0203656e76067072696e746e000103656e76067072696e7473000003030202030404017000000503010001071903066d656d6f7279020004696e69740002056170706c7900030a20020600411010010b17004120100120001000413010012001100041c00010010b0b3f050041040b04504000000041100b0d496e697420576f726c64210a000041200b0e48656c6c6f20576f726c643a20000041300b032d3e000041c0000b020a000029046e616d6504067072696e746e0100067072696e7473010004696e697400056170706c790201300131010b4163636f756e744e616d65044e616d6502087472616e7366657200030466726f6d0b4163636f756e744e616d6502746f0b4163636f756e744e616d6506616d6f756e740655496e743634077265636f7264310002036b65790655496e7436340576616c75650655496e74363401000000572d3ccdcd087472616e736665720200808ac7e4a0b0410369363401036b6579010655496e743634077265636f72643100808ac7e4a0b0410369363401036b6579010655496e743634077265636f726431\"}}\n    thread-0  chain_controller.cpp:1034 apply_message\n\n    {\"trx\":{\"refBlockNum\":126,\"refBlockPrefix\":783788387,\"expiration\":\"2017-11-03T03:37:07\",\"scope\":[\"case1\",\"eos\"],\"readscope\":[],\"messages\":[{\"code\":\"eos\",\"type\":\"setcode\",\"authorization\":[{\"account\":\"case1\",\"permission\":\"active\"}],\"data\":\"0000000080a0b0410000f1010061736d0100000001110460017f0060017e0060000060027e7e00021b0203656e76067072696e746e000103656e76067072696e7473000003030202030404017000000503010001071903066d656d6f7279020004696e69740002056170706c7900030a20020600411010010b17004120100120001000413010012001100041c00010010b0b3f050041040b04504000000041100b0d496e697420576f726c64210a000041200b0e48656c6c6f20576f726c643a20000041300b032d3e000041c0000b020a000029046e616d6504067072696e746e0100067072696e7473010004696e697400056170706c790201300131010b4163636f756e744e616d65044e616d6502087472616e7366657200030466726f6d0b4163636f756e744e616d6502746f0b4163636f756e744e616d6506616d6f756e740655496e743634077265636f7264310002036b65790655496e7436340576616c75650655496e74363401000000572d3ccdcd087472616e736665720200808ac7e4a0b0410369363401036b6579010655496e743634077265636f72643100808ac7e4a0b0410369363401036b6579010655496e743634077265636f726431\"}],\"signatures\":[]}}\n    thread-0  chain_controller.cpp:1072 process_transaction\n\n    {\"trx\":{\"refBlockNum\":126,\"refBlockPrefix\":783788387,\"expiration\":\"2017-11-03T03:37:07\",\"scope\":[\"case1\",\"eos\"],\"readscope\":[],\"messages\":[{\"code\":\"eos\",\"type\":\"setcode\",\"authorization\":[{\"account\":\"case1\",\"permission\":\"active\"}],\"data\":\"0000000080a0b0410000f1010061736d0100000001110460017f0060017e0060000060027e7e00021b0203656e76067072696e746e000103656e76067072696e7473000003030202030404017000000503010001071903066d656d6f7279020004696e69740002056170706c7900030a20020600411010010b17004120100120001000413010012001100041c00010010b0b3f050041040b04504000000041100b0d496e697420576f726c64210a000041200b0e48656c6c6f20576f726c643a20000041300b032d3e000041c0000b020a000029046e616d6504067072696e746e0100067072696e7473010004696e697400056170706c790201300131010b4163636f756e744e616d65044e616d6502087472616e7366657200030466726f6d0b4163636f756e744e616d6502746f0b4163636f756e744e616d6506616d6f756e740655496e743634077265636f7264310002036b65790655496e7436340576616c75650655496e74363401000000572d3ccdcd087472616e736665720200808ac7e4a0b0410369363401036b6579010655496e743634077265636f72643100808ac7e4a0b0410369363401036b6579010655496e743634077265636f726431\"}],\"signatures\":[]}}\n    thread-0  chain_controller.cpp:1043 apply_transaction\n\n    {\"trx\":{\"refBlockNum\":126,\"refBlockPrefix\":783788387,\"expiration\":\"2017-11-03T03:37:07\",\"scope\":[\"case1\",\"eos\"],\"readscope\":[],\"messages\":[{\"code\":\"eos\",\"type\":\"setcode\",\"authorization\":[{\"account\":\"case1\",\"permission\":\"active\"}],\"data\":\"0000000080a0b0410000f1010061736d0100000001110460017f0060017e0060000060027e7e00021b0203656e76067072696e746e000103656e76067072696e7473000003030202030404017000000503010001071903066d656d6f7279020004696e69740002056170706c7900030a20020600411010010b17004120100120001000413010012001100041c00010010b0b3f050041040b04504000000041100b0d496e697420576f726c64210a000041200b0e48656c6c6f20576f726c643a20000041300b032d3e000041c0000b020a000029046e616d6504067072696e746e0100067072696e7473010004696e697400056170706c790201300131010b4163636f756e744e616d65044e616d6502087472616e7366657200030466726f6d0b4163636f756e744e616d6502746f0b4163636f756e744e616d6506616d6f756e740655496e743634077265636f7264310002036b65790655496e7436340576616c75650655496e74363401000000572d3ccdcd087472616e736665720200808ac7e4a0b0410369363401036b6579010655496e743634077265636f72643100808ac7e4a0b0410369363401036b6579010655496e743634077265636f726431\"}],\"signatures\":[]}}\n    thread-0  chain_controller.cpp:244 push_transaction"}

    {"c":500,"msg":"{\"code\":500,\"message\":\"Internal Service Error\",\"details\":\"10 assert_exception: Assert Exception\\ntables.size() == abi.tables.size(): \\n    {}\\n    thread-0  AbiSerializer.cpp:129 setAbi\\n\\n    {\\\"context.msg\\\":{\\\"code\\\":\\\"eos\\\",\\\"type\\\":\\\"setcode\\\",\\\"authorization\\\":[{\\\"account\\\":\\\"case1\\\",\\\"permission\\\":\\\"active\\\"}],\\\"data\\\":\\\"0000000080a0b0410000f1010061736d0100000001110460017f0060017e0060000060027e7e00021b0203656e76067072696e746e000103656e76067072696e7473000003030202030404017000000503010001071903066d656d6f7279020004696e69740002056170706c7900030a20020600411010010b17004120100120001000413010012001100041c00010010b0b3f050041040b04504000000041100b0d496e697420576f726c64210a000041200b0e48656c6c6f20576f726c643a20000041300b032d3e000041c0000b020a000029046e616d6504067072696e746e0100067072696e7473010004696e697400056170706c790201300131010b4163636f756e744e616d65044e616d6502087472616e7366657200030466726f6d0b4163636f756e744e616d6502746f0b4163636f756e744e616d6506616d6f756e740655496e743634077265636f7264310002036b65790655496e7436340576616c75650655496e74363401000000572d3ccdcd087472616e736665720200808ac7e4a0b0410369363401036b6579010655496e743634077265636f72643100808ac7e4a0b0410369363401036b6579010655496e743634077265636f726431\\\"}}\\n    thread-0  chain_controller.cpp:1034 apply_message\\n\\n    {\\\"trx\\\":{\\\"refBlockNum\\\":126,\\\"refBlockPrefix\\\":783788387,\\\"expiration\\\":\\\"2017-11-03T03:37:07\\\",\\\"scope\\\":[\\\"case1\\\",\\\"eos\\\"],\\\"readscope\\\":[],\\\"messages\\\":[{\\\"code\\\":\\\"eos\\\",\\\"type\\\":\\\"setcode\\\",\\\"authorization\\\":[{\\\"account\\\":\\\"case1\\\",\\\"permission\\\":\\\"active\\\"}],\\\"data\\\":\\\"0000000080a0b0410000f1010061736d0100000001110460017f0060017e0060000060027e7e00021b0203656e76067072696e746e000103656e76067072696e7473000003030202030404017000000503010001071903066d656d6f7279020004696e69740002056170706c7900030a20020600411010010b17004120100120001000413010012001100041c00010010b0b3f050041040b04504000000041100b0d496e697420576f726c64210a000041200b0e48656c6c6f20576f726c643a20000041300b032d3e000041c0000b020a000029046e616d6504067072696e746e0100067072696e7473010004696e697400056170706c790201300131010b4163636f756e744e616d65044e616d6502087472616e7366657200030466726f6d0b4163636f756e744e616d6502746f0b4163636f756e744e616d6506616d6f756e740655496e743634077265636f7264310002036b65790655496e7436340576616c75650655496e74363401000000572d3ccdcd087472616e736665720200808ac7e4a0b0410369363401036b6579010655496e743634077265636f72643100808ac7e4a0b0410369363401036b6579010655496e743634077265636f726431\\\"}],\\\"signatures\\\":[]}}\\n    thread-0  chain_controller.cpp:1072 process_transaction\\n\\n    {\\\"trx\\\":{\\\"refBlockNum\\\":126,\\\"refBlockPrefix\\\":783788387,\\\"expiration\\\":\\\"2017-11-03T03:37:07\\\",\\\"scope\\\":[\\\"case1\\\",\\\"eos\\\"],\\\"readscope\\\":[],\\\"messages\\\":[{\\\"code\\\":\\\"eos\\\",\\\"type\\\":\\\"setcode\\\",\\\"authorization\\\":[{\\\"account\\\":\\\"case1\\\",\\\"permission\\\":\\\"active\\\"}],\\\"data\\\":\\\"0000000080a0b0410000f1010061736d0100000001110460017f0060017e0060000060027e7e00021b0203656e76067072696e746e000103656e76067072696e7473000003030202030404017000000503010001071903066d656d6f7279020004696e69740002056170706c7900030a20020600411010010b17004120100120001000413010012001100041c00010010b0b3f050041040b04504000000041100b0d496e697420576f726c64210a000041200b0e48656c6c6f20576f726c643a20000041300b032d3e000041c0000b020a000029046e616d6504067072696e746e0100067072696e7473010004696e697400056170706c790201300131010b4163636f756e744e616d65044e616d6502087472616e7366657200030466726f6d0b4163636f756e744e616d6502746f0b4163636f756e744e616d6506616d6f756e740655496e743634077265636f7264310002036b65790655496e7436340576616c75650655496e74363401000000572d3ccdcd087472616e736665720200808ac7e4a0b0410369363401036b6579010655496e743634077265636f72643100808ac7e4a0b0410369363401036b6579010655496e743634077265636f726431\\\"}],\\\"signatures\\\":[]}}\\n    thread-0  chain_controller.cpp:1043 apply_transaction\\n\\n    {\\\"trx\\\":{\\\"refBlockNum\\\":126,\\\"refBlockPrefix\\\":783788387,\\\"expiration\\\":\\\"2017-11-03T03:37:07\\\",\\\"scope\\\":[\\\"case1\\\",\\\"eos\\\"],\\\"readscope\\\":[],\\\"messages\\\":[{\\\"code\\\":\\\"eos\\\",\\\"type\\\":\\\"setcode\\\",\\\"authorization\\\":[{\\\"account\\\":\\\"case1\\\",\\\"permission\\\":\\\"active\\\"}],\\\"data\\\":\\\"0000000080a0b0410000f1010061736d0100000001110460017f0060017e0060000060027e7e00021b0203656e76067072696e746e000103656e76067072696e7473000003030202030404017000000503010001071903066d656d6f7279020004696e69740002056170706c7900030a20020600411010010b17004120100120001000413010012001100041c00010010b0b3f050041040b04504000000041100b0d496e697420576f726c64210a000041200b0e48656c6c6f20576f726c643a20000041300b032d3e000041c0000b020a000029046e616d6504067072696e746e0100067072696e7473010004696e697400056170706c790201300131010b4163636f756e744e616d65044e616d6502087472616e7366657200030466726f6d0b4163636f756e744e616d6502746f0b4163636f756e744e616d6506616d6f756e740655496e743634077265636f7264310002036b65790655496e7436340576616c75650655496e74363401000000572d3ccdcd087472616e736665720200808ac7e4a0b0410369363401036b6579010655496e743634077265636f72643100808ac7e4a0b0410369363401036b6579010655496e743634077265636f726431\\\"}],\\\"signatures\\\":[]}}\\n    thread-0  chain_controller.cpp:244 push_transaction\"}"}
    thread-0  httpc.cpp:113 call

    {"server":"localhost","port":8888,"path":"/v1/chain/push_transaction","postdata":{"refBlockNum":126,"refBlockPrefix":783788387,"expiration":"2017-11-03T03:37:07","scope":["case1","eos"],"readscope":[],"messages":[{"code":"eos","type":"setcode","authorization":[{"account":"case1","permission":"active"}],"data":"0000000080a0b0410000f1010061736d0100000001110460017f0060017e0060000060027e7e00021b0203656e76067072696e746e000103656e76067072696e7473000003030202030404017000000503010001071903066d656d6f7279020004696e69740002056170706c7900030a20020600411010010b17004120100120001000413010012001100041c00010010b0b3f050041040b04504000000041100b0d496e697420576f726c64210a000041200b0e48656c6c6f20576f726c643a20000041300b032d3e000041c0000b020a000029046e616d6504067072696e746e0100067072696e7473010004696e697400056170706c790201300131010b4163636f756e744e616d65044e616d6502087472616e7366657200030466726f6d0b4163636f756e744e616d6502746f0b4163636f756e744e616d6506616d6f756e740655496e743634077265636f7264310002036b65790655496e7436340576616c75650655496e74363401000000572d3ccdcd087472616e736665720200808ac7e4a0b0410369363401036b6579010655496e743634077265636f72643100808ac7e4a0b0410369363401036b6579010655496e743634077265636f726431"}],"signatures":[]}}
    thread-0  httpc.cpp:117 call
```

## Conclusion
Test Pass.
Tables ABI is stored as dictionary with table name as the key, hence the above sisze mismatch indicates duplication of the table name inside the ABI.
