# Railsコーディング規約

## 行数
- 一行を最大79文字までに抑える。

## インデント
- インデントの幅は2つとする。

良い例:
```ruby
if a < 0
  return true
else
  return false
end
```

悪い例:
```ruby
if a < 0
    return true
else
    return false
end
```

## 空行
- 複数のクラス、メソッドを定義する際は必ず空行を開けること。 

良い例:
```ruby
class Foo
  def self.hoge_1()
    ...
  end

  def hoge_2()
    ...
  end
end

class Bar
  ...
end
```

悪い例:
```ruby
class Foo
  def self.hoge_1()
    ...
  end
  def self.hoge_2()
    ...
  end
end
class Bar
  ...
end
```

## メソッドの定義
- メソッドの定義の際、引数の有無に関わらず括弧をつける。  

良い例:
```ruby
def str(x, y)
  ...
end

def str()
  ...
end
```

悪い例:
```ruby
def str
  ...
end
```

## クラスメソッドの定義
- クラスメソッドを定義する場合は必ず先頭にselfを付ける。  

良い例:
```ruby
class Hoge
  def self.hoge
    ...
  end
end
```

悪い例:
```ruby
class Hoge
  def Hoge.hoge
    ...
  end
end
```

## メソッドの呼び出し方法
- メソッドを呼び出す際は引数の有無に関わらず、必ず括弧をつけること。

良い例:
```ruby
foo(x, y)
Foo.foo(x, y)
foo()
```

悪い例:
```ruby
foo x, y
Foo.foo x, y 
foo
```
