# Poisson FEM Solver
The Poisson equation is the canonical elliptic partial differential equation. For a domain Ω⊂Rn with boundary ∂Ω=ΓD ∪ ΓP, the Poisson equation with particular boundary conditions reads:

−∇⋅(∇u)=f in Ω, u=0 on ΓD, u(0,y)=u(1,y) on ΓP.
Here, f is a given source function. The most standard variational form of Poisson equation reads: find u∈V such that

a(u,v)=L(v)∀ v∈V,
where V is a suitable function space and

a(u,v)=∫Ω ∇u⋅∇v dx,
L(v)=∫Ω fv dx.

Want to develop an FEM solver using fenics subject to the following domain and boundary conditions:

Ω=[0,1]×[0,1] (a unit square)
ΓD={(x,0)∪(x,1)⊂∂Ω} (Dirichlet boundary)
ΓP={(0,y)∪(1,y)⊂∂Ω} (Periodic boundary)
f=xsin(5.0πy)+exp(−((x−0.5)2+(y−0.5)2)/0.02) (source term)
