```c
while (!kthread_should_stop())
	wait_event_interruptible_timeout(
		wq,
		({ bool ready = condition;
		   ready || need_resched(); }),
		HZ);
```
