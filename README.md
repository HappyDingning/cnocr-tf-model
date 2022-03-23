感谢breezedeus开发的cnocr中文ocr模型，项目原地址https://github.com/breezedeus/cnocr

由于工作需要，我将cnocr 1.2.3.1的mxnet模型转换成了tensorflow模型。

我尝试使用现成的迁移方案，如mmdnn或onnx，但是都失败了。

mmdnn出现了我能力范围内无法解决的错误。

onnx不支持linear_before_reset为true的情况，并且由于使用了tensorflow 1.x的API，可能导致模型性能不好。

于是我自己实现了转换，代码已经与模型一同上传。目前只转换了densenet-lite-gru，可以满足大部分场景。如果您想将其他模型转换成tensorflow模型，可以参考densenet-lite-gru目录下的转换代码。
