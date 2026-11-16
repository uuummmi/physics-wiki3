---
title: 線性動量、碰撞與剛體轉動總整理
category: 古典力學
date: 2026-11-14
---

# 線性動量、碰撞與剛體轉動總整理 (Linear Momentum, Collisions and Rotation)

## 📑 本篇目錄 (Table of Contents)
- [1. 線性動量與衝量定理](#1-線性動量與衝量定理)
- [2. 碰撞理論：彈性碰撞與非彈性碰撞](#2-碰撞理論彈性碰撞與非彈性碰撞)
- [3. 質心與多質點系統動力學](#3-質心與多質點系統動力學)
- [4. 剛體繞固定軸轉動與力矩](#4-剛體繞固定軸轉動與力矩)
- [5. 精選例題與必考考點詳解](#5-精選例題與必考考點詳解)
- [6. 專有名詞對照 (Terminology Notes)](#6-專有名詞對照-terminology-notes)

---

## 1. 線性動量與衝量定理
### (1) 線性動量 (Linear Momentum, $\vec{p}$)
- **定義**：物體質量與速度的乘積，為一向量，方向與速度相同。
  $$\vec{p} \equiv m\vec{v}$$
- **單位**：$\text{kg}\cdot\text{m/s}$（維度為 $[M][L][T]^{-1}$）。
- **與牛頓第二定律的連結**：當質量固定時，淨外力等於動量對時間的變化率。
  $$\sum\vec{F} = m\vec{a} = m\frac{d\vec{v}}{dt} = \frac{d(m\vec{v})}{dt} = \frac{d\vec{p}}{dt}$$

### (2) 衝量與衝量動量定理 (Impulse-Momentum Theorem, $\vec{I}$)
- **定義**：力對時間的積分，等於力－時間曲線下的面積。
  $$\vec{I} \equiv \int_{t_i}^{t_f} \sum\vec{F} \, dt = (\sum\vec{F})_{\text{avg}} \Delta t$$
- **衝量動量定理**：粒子動量的變化量等於作用在其上的淨外力衝量。
  $$\Delta\vec{p} = \vec{p}_f - \vec{p}_i = \vec{I}$$

---

## 2. 碰撞理論：彈性碰撞與非彈性碰撞
在孤立系統中（不受外力或外力合力為零），碰撞前後總動量恆守恆（$\sum\vec{p}_i = \sum\vec{p}_f$）。根據機械能是否守恆，可分為三大類：

* **彈性碰撞 (Elastic Collisions)**：動量與總動能皆守恆（$E_{ki} = E_{kf}$）。在一維彈性碰撞中，相對分離速率等於相對接近速率：
  $$v_{1i} - v_{2i} = -(v_{1f} - v_{2f})$$
* **非彈性碰撞 (Inelastic Collisions)**：動量守恆，但動能不守恆（部分能量因摩擦、形變轉為熱能或聲能）。
* **完全非彈性碰撞 (Perfect Inelastic Collisions)**：碰撞後兩物體黏合在一起（$v_{1f} = v_{2f} = v_f$），動能損失達到最大。
  $$\vec{v}_f = \frac{m_1\vec{v}_{1i} + m_2\vec{v}_{2i}}{m_1 + m_2}$$

---

## 3. 質心與多質點系統動力學
### (1) 質心座標 (Center of Mass, CM)
- **離散質點系統**：
  $$x_{\text{CM}} = \frac{\sum m_i x_i}{M}, \quad y_{\text{CM}} = \frac{\sum m_i y_i}{M}, \quad z_{\text{CM}} = \frac{\sum m_i z_i}{M}$$
- **連續質體積分**：
  $$\vec{r}_{\text{CM}} = \frac{1}{M}\int \vec{r} \, dm = \frac{1}{M}\int \vec{r}\rho \, dV$$

### (2) 系統總動量與外力
- 系統總動量等於總質量乘以質心速度：$\vec{P}_{\text{tot}} = M\vec{v}_{\text{CM}}$。
- **系統運動方程式**：作用在系統上的淨外力等於總質量乘以質心加速度。
  $$\sum\vec{F}_{\text{ext}} = M\vec{a}_{\text{CM}} = \frac{d\vec{P}_{\text{tot}}}{dt}$$
- 當 $\sum\vec{F}_{\text{ext}} = 0$ 時，系統總動量守恆（$\vec{P}_{\text{tot}} = \text{constant}$）。

---

## 4. 剛體繞固定軸轉動與力矩
當物體大小不可忽略、視為剛體時，其轉動定律與直線運動完全對應（$x \to \theta, v \to \omega, m \to I$）：
- **轉動運動學**：$\omega_f = \omega_i + \alpha t$、$\theta_f = \theta_i + \omega_i t + \frac{1}{2}\alpha t^2$、$\omega_f^2 = \omega_i^2 + 2\alpha\Delta\theta$。
- **力矩 (Torque)**：$\tau = rF\sin\phi = Fd$（力臂 $d$ 為轉軸到力作用線的垂直距離）。
- **轉動牛頓第二定律**：$\sum\tau_{\text{ext}} = I\alpha$，其中轉動慣量 $I = \sum m_i r_i^2 = \int r^2 dm$。
- **平行軸定理**：$I = I_{\text{CM}} + MD^2$。
- **轉動動能與純滾動**：$K_R = \frac{1}{2}I\omega^2$，純滾動時滿足 $v_{\text{CM}} = R\omega$。

---

## 5. 精選例題與必考考點詳解

> **【例題 1】一維彈性碰撞的特殊質量情況**
> - **題目敘述**：兩個質量分別為 $m_1$ 與 $m_2$ 的物體進行一維彈性碰撞，若目標物靜止（$v_{2i} = 0$），試討論 $m_1 = m_2$ 以及 $m_1 \gg m_2$ 時的末速度。
> - **🎯 必考考點解析**：
>   1. 彈性碰撞同時滿足「動量守恆」與「動能守恆」。
>   2. 常用於粒子物理與力學碰撞題型的極限討論。
> - **💡 詳細詳解**：
>   碰撞後兩物體末速度公式為：
>   $$v_{1f} = \frac{m_1 - m_2}{m_1 + m_2}v_{1i}, \quad v_{2f} = \frac{2m_1}{m_1 + m_2}v_{1i}$$
>   - **情況一（質量相等 $m_1 = m_2$）**：$v_{1f} = 0$，$v_{2f} = v_{1i}$（發生完全速度交換，例如牛頓擺）。
>   - **情況二（重球撞輕球 $m_1 \gg m_2$）**：$v_{1f} \approx v_{1i}$，$v_{2f} \approx 2v_{1i}$（輕球被彈飛至兩倍初速）。

---

> **【例題 2】均勻半圓形細線的質心計算**
> - **題目敘述**：一條質量為 $M$、半徑為 $R$ 的均勻半圓形細線，置於座標系中（對稱於 $y$ 軸），求其質心座標 $\vec{r}_{\text{CM}}$。
> - **🎯 必考考點解析**：
>   1. 利用對稱性（$x_{\text{CM}} = 0$）。
>   2. 善用微元法（$dm = \lambda R d\theta$）與三角函數積分。
> - **💡 詳細詳解**：
>   微元位置向量 $\vec{r} = R\cos\theta\,\hat{i} + R\sin\theta\,\hat{j}$，線密度 $\lambda = \frac{M}{\pi R}$。
>   $$y_{\text{CM}} = \frac{1}{M}\int (R\sin\theta)\lambda R\,d\theta = \frac{R^2\lambda}{M}\int_{0}^{\pi}\sin\theta\,d\theta = \frac{R^2(\frac{M}{\pi R})}{M}[-\cos\theta]_0^{\pi} = \frac{2R}{\pi}$$
>   故質心座標為 $\vec{r}_{\text{CM}} = \frac{2R}{\pi}\hat{j}$。

---

## 6. 專有名詞對照 (Terminology Notes)
- **Linear Momentum**：線性動量
- **Impulse**：衝量（力對時間的累積效果）
- **Elastic / Inelastic Collision**：彈性碰撞 / 非彈性碰撞
- **Center of Mass (CM)**：質心
- **Torque**：力矩
- **Moment of Inertia**：轉動慣量
- **Parallel-Axis Theorem**：平行軸定理
- **Pure Rolling Motion**：純滾動運動（無滑動滾動）