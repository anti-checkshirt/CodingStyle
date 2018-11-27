# Railsコーディング規約

## 行数
- 一行を最大79文字までに抑える。

## インデント
- インデントの幅は2つとする。
```ruby
# 良い例
if a < 0
    return true
else
    return false
end

# 悪い例
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
	def hoge_1()
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
	def hoge_1()
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
