Serenity "batch" issue
===

There are 4 tests in 4 classes. Configuration: `serenity.batch.count = 2`.

Now look at this:

```
$ mvn integration-test -Dserenity.batch.number=1

Tests run: 0, Failures: 0, Errors: 0, Skipped: 0

```

```
$ mvn integration-test -Dserenity.batch.number=2

Tests run: 4, Failures: 0, Errors: 0, Skipped: 0

```

Batches should run 2 tests each, but somehow first one runs none and second takes all.