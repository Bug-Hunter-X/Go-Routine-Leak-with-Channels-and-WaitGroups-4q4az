# Go Routine Leak with Channels and WaitGroups

This repository demonstrates a common error in Go concurrent programming involving channels and `sync.WaitGroup`. The program deadlocks due to an improper use of `WaitGroup.Done()`, leading to a goroutine leak. 

The `bug.go` file contains the erroneous code. The `bugSolution.go` file provides the corrected version.

## Bug Description

A goroutine leak occurs when a goroutine is launched but never completes. In this example, both the sending and receiving goroutines never complete, leading to a deadlock.