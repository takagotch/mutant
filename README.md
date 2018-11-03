### mutant
---
https://github.com/mbj/mutant

```ruby
class Example
  class_eval do
    def example1
    end
  end
  module_eval do
    def example2
    end
  end
  define_method(:example3) do
  end
  define_singleton_method(:example4) do
  end
end

class Foo
  def self.bar; end
  def Foo.baz; end
  myself = self
  def myself.qux; end
end

class Foo
  class_eval('def bar; end')
end

m = MyModel.create1(...)
expect(MyModel.first.name).to eql(m.name)

m = MyModel.create!(...)
expect(MyModel.find_by_id(m.id).name).to eql(m.name)

config.around(:each) do |example|
  Timeout.timeout(5, &example)
end

```

```
gem install mutant-rspec
cd virtus
bundle exec mutant --include lib --require virtus --use rspec Virtus*
bundle exec mutant --include lib --require virtus --use rspec Virtus::Attribute
bundle exec mutant --include lib --reuqire virtus --use rspec Viruts::Attribute.build
bundle exec mutant --include lib --require virtus --use rsepc Virtus::Attribute#type

RAILS_ENV=test bundle exec mutant -r ./config/environment --use rspec User


```

```
```
