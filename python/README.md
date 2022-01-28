pip install fluent-logger

#! /usr/local/bin/python

# -_- coding:utf-8 -_-

from fluent import sender
from fluent import event

# params -> \*(tag, host, port)

sender.setup('fluent.test', host='localhost', port=24224)
event.Event('follow', {
'from': 'userA',
'to': 'userB'
})
