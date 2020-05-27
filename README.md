# Zero-determinant strategies
２人プレイヤーi$\in\{X,Y\}$の繰り返し囚人のジレンマゲームを考える．ゲームのそれぞれのラウンドで，プレイヤーは，協力（C）か裏切り（D）の行動を選ぶ．プレイヤーの利得は，自分と相手の行動によって決まる．利得行列は,
で与えられる．繰り返し囚人のジレンマゲームを考えているので，$T>R>P>S$と$2R>T+S$を仮定する．このゲームを無限期にわたって繰り返す．プレイヤーの戦略は，memory-one戦略であると仮定する．この戦略は，前回の自分と相手の行動から今回の行動を確率的に決定する．したが
$$
\boldsymbol{p} =(p_{\rm CC},p_{\rm CD},p_{\rm DC},p_{\rm DD})
$$
と定義する（$0\le p_i\le 1, \in \{1,2,3,4 \}$）．$p_1$は前回のラウンドで$X$と$Y$が協力したとき，今回，$X$が協力する確率である．$p_2$は前回のラウンドで$X$が協力で，$Y$が裏切りのとき，今回，$X$が協力する確率である．$p_3$は前回のラウンドで$X$が裏切り，$Y$が協力したとき，今回，$X$が協力する確率である．$p_4$は前回のラウンドで$X$と$Y$が裏切りであったとき，今回，$X$が協力する確率である．$p_0$は初期ラウンドで協力する確率である．同様に，プレイヤー$Y$の戦略は，
\begin{equation}
	\boldsymbol{q} =(q_{CC},q_{CD},q_{DC},q_{DD})
\end{equation}
と定義する．繰り返しゲームの初期ラウンドを$t=0$とする．また，プレイヤーの戦略は記憶1戦略を採用しているので，$t\ (t \ge 0)$期目の2人プレイヤーのゲームの状態は，
\begin{equation}
	\boldsymbol{v}(t)=(v_1,v_2,v_3,v_4)
\end{equation}
で与えられる．$v_1(t)$は，$t$期目で，$X$と$Y$が両方ともCであった確率，$v_2(t)$は，$X$がC，$Y$がDであった確率，$v_3(t)$は，$X$がD，$Y$がCであった確率，$v_4(t)$は，$X$がD，$Y$がDであった確率である．また，初期状態は式より
\begin{equation}
	\boldsymbol{v}(0)=(p_0 q_0,p_0 (1-q_0),(1-p_0)q_0,(1-p_0)(1-q_0))
\end{equation}
で与えられる．プレイヤー$X$の利得行列を$\boldsymbol{S_X}=(R,S,T,P)$とする（プレイヤー$X$の利得行列を$\bm S_Y=(R,T,S,P)$とする）と，$t$期目での利得は，$\boldsymbol{v}(t)\bm S_X^T$で計算できる．したがって，プレイヤー$X$の割引平均利得は，
\begin{equation}
	s_X=(1-\delta)\sum^{\infty} _{t=0} \delta^t \bm v(t) \bm S_X^T
\end{equation}
となる（$0< \delta < 1$）．また，ゲームの状態遷移行列は，
\begin{equation}
  M = \left(
    \begin{array}{cccc}
      p_1 q_1 & p_1(1-q_1) & (1-p_1)q_1 &(1-p_1)(1-q_1)\\
      p_2 q_3 & p_2(1-q_3) & (1-p_2)q_3 &(1-p_2)(1-q_3)\\
      p_3 q_2 & p_3(1-q_2) & (1-p_3)q_2 &(1-p_3)(1-q_2)\\
      p_4 q_4 & p_4(1-q_4) & (1-p_4)q_4 &(1-p_4)(1-q_4)
    \end{array}
  \right)
\end{equation}
である．遷移行列$M$のそれぞれの行と列は，前回のゲームの状態と次の状態を表している．よって，$t$期目でのゲームの状態は，遷移行列$M$を使うと，
\begin{equation}
	\bm v(t)=\bm v(0) M^t
\end{equation}
と表せる．これをに代入すると，
\begin{equation}
\begin{split}
	s_X&=(1-\delta)\boldsymbol{v}(0)\sum^{\infty}_{t=0} (\delta M)^t \boldsymbol{S_X}^T \\
	      &=(1-\delta)\boldsymbol{v}(0)(I-\delta M)^{-1}\boldsymbol{S_X}^T
\end{split}
\end{equation}
が得られる．ここで，
\begin{eqnarray}
	\bm v^T \equiv (v_1,v_2,v_3,v_4)
	=(1-\delta)\bm v(0)(I-\delta M)^{-1}
\end{eqnarray}
とおく．
\begin{equation}
  \bm M_0 \equiv \left(
    \begin{array}{cccc}
      p_0 q_0 & p_0(1-q_0) & (1-p_0)q_0 &(1-p_0)(1-q_0)\\
      p_0 q_0 & p_0(1-q_0) & (1-p_0)q_0 &(1-p_0)(1-q_0)\\
      p_0 q_0 & p_0(1-q_0) & (1-p_0)q_0 &(1-p_0)(1-q_0)\\
      p_0 q_0 & p_0(1-q_0) & (1-p_0)q_0 &(1-p_0)(1-q_0)
    \end{array}
  \right)
\end{equation}
$v_1+v_2+v_3+v_4=1$であるので，$\bm v(0)=\bm v^T M_0$が成り立つ．ついて，$\bm v(0)=\bm v^T M_0$を代入し，両辺に右から$(I-\delta M)$をかけると，
\begin{equation}
	\bm v^T	(I-\delta M)=\bm v^T M_0
\end{equation}
が得られる．と$M^\prime \equiv \delta M+(1-\delta)M_0-I$とする．$Adj(M^\prime)$の4行目をベクトルとして，$\bm u$とおくと，Press-Dysonが行った操作によって，$\bm u$と任意のベクトル$\bm f=(f_1,f_2,f_3,f_4)$の内積は，
\begin{equation}
\bm u\cdot \bm f=
  \left|
    \begin{array}{cccc}
      \delta p_1 q_1-1 +p_0 q_0(1-\delta)& \delta p_1-1 +p_0(1-\delta)& \delta q_1-1 +q_0 (1-\delta)& f_1\\
            \delta p_2 q_3+p_0 q_0(1-\delta)& \delta p_2-1+p_0(1-\delta)& \delta q_3  +q_0 (1-\delta)& f_2\\
      \delta p_3 q_2+p_0 q_0(1-\delta)& \delta p_3  +p_0(1-\delta)& \delta q_2-1+q_0 (1-\delta)& f_3\\
      \delta p_4 q_4+p_0 q_0(1-\delta)& \delta p_4  +p_0(1-\delta)& \delta q_4  +q_0 (1-\delta)& f_4
    \end{array}
  \right|
 \equiv D(\bm p,\bm q,\bm f)
\end{equation}
と書ける．さらに，を正規化すると，平均分布$\bm v$と$\bm f$の内積が得られる．したがって，プレイヤーXの期待利得は
\begin{equation}
s_X=\bm v \cdot \bm S_X=\frac{\bm u \cdot \bm S_X}{\bm u \cdot \bm 1}
   =\frac{D(\bm p,\bm q,\bm S_X)}{D(\bm p,\bm q,\bm 1)}
\end{equation}
となる．同様に，プレイヤーYでは，
\begin{equation}
s_Y=\bm v \cdot \bm S_Y=\frac{\bm u \cdot \bm S_Y}{\bm u \cdot \bm 1}
   =\frac{D(\bm p,\bm q,\bm S_Y)}{D(\bm p,\bm q,\bm 1)}
\end{equation}
となる．$s_X$と$s_Y$を線形結合すると，行列式の性質から
\begin{equation}
	\alpha s_X +\beta s_Y +\gamma= \frac{D(\bm p,\bm q,\alpha \bm S_X+\beta \bm S_Y+\gamma \bm 1)}{D(\bm p,\bm q,\bm 1)}
\end{equation}
と表せる．ここで，相手の戦略にかかわらず，$D(\bm p,\bm q,\alpha \bm S_X+\beta \bm S_Y+\gamma \bm 1)=0$を成り立たせることができたとき，
\begin{equation}
	\alpha s_X +\beta s_Y +\gamma= 0
\end{equation}
の関係を強いることができる．つまり，自分と相手の利得の期待値の関係が線形にさせることができる．また，式の右辺の分子は以下の行列式の形で与えられる．
\begin{equation}
\begin{split}
&D(\bm p,\bm q,\alpha \bm S_X+\beta \bm S_Y+\gamma \bm 1)=\\
&
  \left|
    \begin{array}{cccc}
      \delta p_1 q_1-1 +p_0 q_0(1-\delta)& \delta p_1-1 +p_0(1-\delta)& \delta q_1-1 +q_0 (1-\delta)& \alpha R+\beta R +\gamma\\
      \delta p_2 q_3+p_0 q_0(1-\delta)& \delta p_2-1+p_0(1-\delta)& \delta q_3  +q_0 (1-\delta)& \alpha S+\beta T +\gamma\\
      \delta p_3 q_2+p_0 q_0(1-\delta)& \delta p_3  +p_0(1-\delta)& \delta q_2-1+q_0 (1-\delta)& \alpha T+\beta S +\gamma\\
      \delta p_4 q_4+p_0 q_0(1-\delta)& \delta p_4  +p_0(1-\delta)& \delta q_4  +q_0 (1-\delta)& \alpha P+\beta P +\gamma
    \end{array}
  \right|
\end{split}
\end{equation}
よって，Zero-determinant戦略は，
\begin{equation}
\begin{split}
      \delta p_1-1+p_0(1-\delta)&=\alpha R+\beta R+\gamma \\
      \delta p_2-1+p_0(1-\delta)&=\alpha S+\beta T+\gamma \\
      \delta p_3+p_0(1-\delta)  &=\alpha T+\beta S+\gamma \\
      \delta p_4+p_0(1-\delta)  &=\alpha P+\beta P+\gamma
\end{split}
\end{equation}
で与えられる．