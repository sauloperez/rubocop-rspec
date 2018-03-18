You need to tell RuboCop to load the RSpec extension. There are three
ways to do this:

### RuboCop configuration file

Put this into your `.rubocop.yml`.

```
require: rubocop-rspec
```

Now you can run `rubocop` and it will automatically load the RuboCop RSpec
cops together with the standard cops.

### Command line

```bash
rubocop --require rubocop-rspec
```

### Rake task

```ruby
RuboCop::RakeTask.new do |task|
  task.requires << 'rubocop-rspec'
end
```

### Code Climate

rubocop-rspec is available on Code Climate as part of the rubocop engine. [Learn More](https://codeclimate.com/changelog/55a433bbe30ba00852000fac).
