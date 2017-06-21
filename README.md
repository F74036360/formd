# Final Exam’s good friend

# Hello, everyone
- This is  ***private document***. Before distributing, please think twice.


- 現在放棄，暑假就開始了 ^.<
- 勇士都被騎士逆轉了，你覺得你期末考還有救嗎？
- 放棄吧，這只是份空文件！認真讀書吧…





















































































- 題目：https://drive.google.com/open?id=0B6V4b8ue-xhcWnRLS0VqVGpfaW8
- 畫 NPDA / DPDA / Turing Machine 時，可以利用 [Draw.io](http://draw.io) 繪圖。
- Latex 語法請參考 [此文件](http://mohu.org/info/symbols/symbols.htm)。
# 2013 Final Exam
## Basic Concepts ( 30 pts / 3 pt each )
1. $$(a+b)$$ is one of regular languages, and $$(a+b)^{*}$$ is one of context-free languages.
    TRUE
    $$S \to SS\ |\ a\ |\ b\ |\ \lambda$$


2. Given a context-free grammar $$G=\{V, T, S, P\}$$, a variable$$A$$ is called useful if and only if at least a string $$w \in L(G)$$ which can be derived as follows:
  $$S \Longrightarrow ... \Longrightarrow xAy \Longrightarrow ... \Longrightarrow w,\ where\ x,y \in (V \cup T)^{*}$$
    TRUE
    Trivial, Ch06P15


3. The following NPDA can accept $$L = \{wcw^{R}\ :\ w \in \{a, b\}^{*}\}$$:
https://d2mxuefqeaa7sj.cloudfront.net/s_A7CCBB429C0BF8203C1CEE57DC1AC1F253210EA0E7038DDC055EEB01169991E0_1466571163930_file.png

    FALSE
    最後一條 (λ, λ, λ) 改成 (λ, z, z) 即可。  
    否則可接受 abcb。


4. We can describe the set of all properly nested parenthesis structures for the common programming language, e.g. (()) and () () (), by the grammar with productions:
  $$S \to aSb\ |\ SS\ |\ \lambda$$
    TRUE
    Trivial, Ch05P19


5. The transition function of turing machine $$M$$ is modeled as three tuples: $$(x, y, z)$$, where $$x$$ indicates the symbol read from the tape, $$y$$ indicates the symbol written to the tape, and $$x, y \in \Sigma \cup \lambda$$. In addition, $$z$$ indicates the Read-Write head will either move left or move right.
    FALSE
    Trivial, Ch09P21
    Turing Machine don't accept lambda transition.
    BTW, $$x, y \in \Gamma$$


6. In a DPDA, if $$\delta (q, \lambda, b)$$ is not empty, then $$\delta(q, c, b)$$ must be empty for every $$c \in \Sigma$$.
    TRUE
    Trivial, Ch07bP76


7. Given a turing machine, a string $$w$$ is accepted if it can be completely walked from the head to the end of $$w$$.
    FALSE
    Last state must be a final state


8. Suppose that we have a push-down automaton $$M$$. If the string $$w$$ is consumed completely and the last state is a final state of $$M$$, we say $$w$$ is accepted by $$M$$ without the need of checking the  content in the stack.
    TRUE
    Trivial, Ch07aP34


9. Note that $$L_{1}=a^{n}b^{n}c^{m}$$ and$$L_{2}=a^{n}b^{m}c^{m}$$ are both context-free. We have $$L_{3}=L_{1} \cap L_{2}$$ and $$L_{3}$$ is also context-free.
    FALSE
    $$L_{3}=a^{n}b^{n}c^{n}$$ is not context-free


10. In this semester, we have checked the attendance only one time (except for two exams).
    3
    If not, see you next year :)
## Advanced Questions ( 70 pts / 10 pt each )
1. Show that the following grammar is ambiguous.
  $$S \to aSbS\ |\ bSaS\ |\ \lambda$$
    $$S \to aSbS \to abSaSbS \to abaSbS \to ababS \to abab$$$$S \to aSbS \to aSbaSbS \to abaSbS \to ababS \to abab$$$$$$


2. Transform the grammar with productions:
  $$S \to abAB$$
  $$A \to bAB\ |\ \lambda$$
  $$B \to BAa\ |\ A\ |\ \lambda$$
  into CNF. (Please simplify the grammar first!)
    1. Simplify
      1.1. Remove Nullable Variable
        $$S \to abAB\ |\ abA\ |\ abB\ |\ ab$$
        $$A \to bAB\ |\ bA\ |\ bB\ |\ b$$
        $$B \to BAa\ |\ Aa\ |\ Ba\ |\ a\ |\ A$$
      1.2. Remove Unit productions
        $$S \to abAB\ |\ abA\ |\ abB\ |\ ab$$
        $$A \to bAB\ |\ bA\ |\ bB\ |\ b$$
        $$B \to BAa\ |\ Aa\ |\ Ba\ |\ a$$
        +
        $$B \to bAB\ |\ bA\ |\ bB\ |\ b$$
        =
        $$S \to abAB\ |\ abA\ |\ abB\ |\ ab$$
        $$A \to bAB\ |\ bA\ |\ bB\ |\ b$$
        $$B \to bAB\ |\ bA\ |\ bB\ |\ b\ |\ BAa\ |\ Aa\ |\ Ba\ |\ a$$
        $$\Longrightarrow$$
        $$S \to abAB\ |\ abA\ |\ abB\ |\ ab$$
        $$A \to bAB\ |\ bA\ |\ bB\ |\ b$$
        $$B \to bAB\ |\ bA\ |\ bB\ |\ b\ |\ BAa\ |\ Aa\ |\ Ba\ |\ a$$
      1.3. Remove Useless productions (No change)
        $$S \to abAB\ |\ abA\ |\ abB\ |\ ab$$
        $$A \to bAB\ |\ bA\ |\ bB\ |\ b$$
        $$B \to bAB\ |\ bA\ |\ bB\ |\ b\ |\ BAa\ |\ Aa\ |\ Ba\ |\ a$$
    2. Please see Reference Answer for 2012


3. Construct an NPDA that accepts the following language on {a,b,c} (use an NPDA with 2 states):
  $$L = \{ w\ :\ n_{a}(w) + n_{b}(w) = n_{c}(w) \}$$
https://d2mxuefqeaa7sj.cloudfront.net/s_A7CCBB429C0BF8203C1CEE57DC1AC1F253210EA0E7038DDC055EEB01169991E0_1466599234851_Untitled+Diagram.png



4. Construct an NPDA corresponding to the grammar:
  $$S \to aABB\ |\ aAA$$
  $$A \to aBB\ |\ a$$
  $$B \to bBB\ |\ A$$
https://scontent-tpe1-1.xx.fbcdn.net/v/t34.0-12/13514479_10210263999863546_599444961_n.png?oh=50cf0e06f5e619f0b43db2855773982a&oe=576C9CA4



5. Using the pumping lemma to prove that $$L = \{a^{n}b^{2n}c^{n}\ :\ n \ge 0\}$$ is not a context-free language.
    Please see Reference Answer for 2012


6. Construct a turing machine that accepts the following languages on $$L = \{a^{n}b^{n+1}\ :\ n \ge 1\}$$.
https://d2mxuefqeaa7sj.cloudfront.net/s_A7CCBB429C0BF8203C1CEE57DC1AC1F253210EA0E7038DDC055EEB01169991E0_1466607861313_file.png

7. Fill the following languages into the language hierarchy ( If $$L_{i}$$ is a regular language and also a context-free language please $$L_{i}$$ in the set of regular languages):
  $$See\ \ pdf\ \ by\ \ yourself$$
    Please see Reference Answer for 2012 EXCEPT $$L_{10}$$
    $$L_{10}$$ is not CFG.
# 2012 Final Exam
## Basic Concepts
1. Same with 2013–1.


2. The set of regular language is a subset of context-free language.
    TRUE


3. A context-free grammar is linear.
    FALSE


4. Given a context-free grammar $$G = \{V, T, S, P\}$$, we say each rule in $$P$$ will be of the form $$A \to x$$, where $$x \in (V \cup T)^{*}$$.
    TRUE


5. Same with 2013–4.


6. Let $$G=(V, T, S, P)$$ be a CFG. If $$t_{G}$$ is any partial derivation tree for $$G$$ whose root is labeled $$S$$, then the leftmost scan of leaf nodes of $$t_{G}$$ yields a string (only terminals) accepted by $$G$$.
    FALSE
    Not any partial derivation tree will yeild a string.
    It may be senential form or string.


7. Same with 2013–3


8. Given a push-down automaton, transitions for checking acceptance of the string can be continued when the stack is empty.
    FALSE
    If it didn't reach final state before emptying stack,
      the automaton will halt and reject.


9. In a PDA, a string is accepted if there is a computation such that all the input is consumed and the last state is the final state.
    TRUE


10. Same with 2013–6


11. NPDAs and DPDAs have the same computation power.
    FALSE


12. The pumping lemma can be used to prove that a language is a context-free languages.
    FALSE


13. Python codes can be executed without the need of machine dependent pre-compilation.
    TRUE
    Python will generate bytecode at the first running time.
    But this bytecode will be plateform-independent, but version-dependent.


14. For using the internet functionality in python, you should import the “re” library.
    FALSE
    "re" library is for Regular Expression.


15. The following python code will be compiled successfully.
  def perm(l):
    for i in range(len(i)):
    s = l[:i] + l[i+1:]
    p = perm(l[:i] + l[i+1:])
    for x in p:
    r.append(l[i:i+1] + x)
    return r
    FALSE
    Invalid syntax.
## Advanced Options

**Please see Reference Answer for 2012**

# Others
## Turing Machine Practice
- $$L = a^{n} b^{n} c^{n}$$
https://d2mxuefqeaa7sj.cloudfront.net/s_A7CCBB429C0BF8203C1CEE57DC1AC1F253210EA0E7038DDC055EEB01169991E0_1466577087989_TManbncn.png



- $$f(x, y)=\{1\ \ if\ \ x \gt y,\ \ 0\ \ if\ \ x \le y\}$$
https://d2mxuefqeaa7sj.cloudfront.net/s_A7CCBB429C0BF8203C1CEE57DC1AC1F253210EA0E7038DDC055EEB01169991E0_1466581152663_TMxgty.png



- $$L=\{w\ :\ n_{a}(w) = n_{b}(w) + 1\}$$
https://d2mxuefqeaa7sj.cloudfront.net/s_A7CCBB429C0BF8203C1CEE57DC1AC1F253210EA0E7038DDC055EEB01169991E0_1466653628961_file.png



- Multiplies two positive integers in unary notation


- Even-length binary palindromes


































































